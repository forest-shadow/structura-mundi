---
aliases:
  - Display Technologies Structure Proposal
  - Структура ветки Display Technologies
note_type: article
area: computer-science
domain: computer-architecture
section: display-technologies
parent:
status: draft
related:
  - "[[Computer Architecture]]"
  - "[[Display Technologies]]"
  - "[[Liquid Crystal Display]]"
tags: []
---

# Display Technologies Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для ветки `Display Technologies`, в которую естественно помещается рассмотрение понятия `Liquid Crystal Display`, по правилам `Principia Rerum`.

## Выбранная оптика

- `area: computer-science`
- `domain: computer-architecture`
- `section: display-technologies` (новый локальный кластер)

Почему так:

- `Liquid Crystal Display` в этой оптике лучше понимать как аппаратную технологию визуального вывода, а не как тему из `Operating Systems`, `Web Platform` или `Human-Computer Interaction`;
- отдельный новый `domain` вроде `display-engineering` пока преждевременен: для этого в vault еще нет устойчивого корпуса соседних display-веток;
- внутри `Computer Architecture` уже есть место для hardware-тем, которые описывают, как машина реализует вычисление и вывод результата на физическом устройстве.

## Рекомендуемая иерархия

```text
Computer Science
└── Computer Architecture
    └── Display Technologies
        └── Liquid Crystal Display
```

## Почему структура именно такая

- `Display Technologies` оправдан как section-level `overview`, потому что тема уже собирает потенциальный кластер sibling-технологий, а не одну isolated definition-note.
- `Liquid Crystal Display` пока лучше держать обычной `article`, потому что одной темы LCD еще недостаточно для отдельного LCD-specific overview с дочерними notes.
- Глубже этой вложенности идти пока не стоит: для `LCD panel types`, `backlighting families`, `refresh behavior` и `manufacturing variants` еще нет устойчивого корпуса.

## Что не стоит создавать заранее

- отдельный `domain` вроде `display-engineering` или `display-hardware`, пока рядом нет устойчивого корпуса соседних веток;
- отдельный overview вроде `Flat-Panel Displays`, если в нем пока нет самостоятельных sibling-кластеров рядом с `Liquid Crystal Display`;
- отдельные canonical notes для `TN LCD`, `IPS LCD`, `VA LCD`, `Mini-LED Backlight` и других уточнений, пока по ним не накопился самостоятельный материал;
- тематические template-файлы под display hardware: по `Principia Rerum` здесь должны оставаться только канонические `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
├── C/
│   └── Computer Architecture.md
├── D/
│   └── Display Technologies.md
└── L/
    └── Liquid Crystal Display.md
```

Логическая ветка затем должна собираться через `parent`, а не через физические подпапки.

## Что уже создано в Inbox

- `[[Display Technologies]]`
- `[[Liquid Crystal Display]]`

## Что стоит раскрыть дальше

- [ ] Подтвердить `section: display-technologies`
- [ ] Решить, когда рядом с `Liquid Crystal Display` нужны `OLED`, `CRT` и `E Ink`
- [ ] Уточнить, когда внутри ветки уместны notes про panel types и backlighting
- [ ] Проверить `related`
