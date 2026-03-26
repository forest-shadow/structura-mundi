---
aliases:
  - Golang Netpoller Structure Proposal
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Scheduler]]"
status: draft
related:
  - "[[Go Netpoller]]"
  - "[[Go Scheduler]]"
  - "[[Go Concurrency Model]]"
  - "[[Go Goroutines]]"
tags: []
---

# Go Netpoller Structure Proposal

## Краткое определение

Предлагаемая ветка для `Go Netpoller` выделяет сетевой опросчик runtime Go в самостоятельную каноническую статью внутри scheduler-подветки.

## Почему тема заслуживает отдельной статьи

- `Netpoller` регулярно всплывает при объяснении того, как Go совмещает большое количество сетевых ожиданий с небольшим числом OS threads.
- Это устойчивый механизм runtime, а не одноразовая деталь реализации.
- Тема достаточно узкая, чтобы остаться `article`, и достаточно важная, чтобы не теряться внутри общей заметки `[[Go Scheduler]]`.

## Рекомендуемая иерархия

```text
Go
└── Go Concurrency Model
    ├── Go Goroutines
    ├── Go Channels
    └── Go Scheduler
        ├── Go Scheduler GMP Model
        ├── Go Scheduler Work Stealing
        ├── Go Scheduler Preemption
        └── Go Netpoller
```

## Почему структура именно такая

- `Go Netpoller` лучше держать под `[[Go Scheduler]]`, потому что он объясняет один из источников пробуждения runnable goroutines.
- Не стоит делать из него отдельный верхнеуровневый `overview`: глубина ветки тогда станет избыточной.
- Каноническое имя лучше зафиксировать как `Go Netpoller`, а `Netpoller` оставить в `aliases`, чтобы избежать неоднозначности с одноимёнными механизмами вне Go.

## Что не стоит добавлять прямо сейчас

- Не стоит сразу дробить тему на `epoll`, `kqueue` и `IOCP` как отдельные статьи.
- Не стоит превращать заметку в каталог runtime-исходников без устойчивых энциклопедических границ.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
└── G/
    └── Go Netpoller.md
```

## Что уже создано в Inbox

- `[[Go Netpoller]]`

## Что стоит раскрыть дальше

- [ ] Проверить, нужен ли отдельный article про `sysmon`
- [ ] Уточнить связь между `Go Netpoller` и runtime timers
- [ ] Проверить `related`
