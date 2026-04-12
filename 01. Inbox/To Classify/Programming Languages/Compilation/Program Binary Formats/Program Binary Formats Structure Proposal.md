---
aliases:
  - Binary Formats Structure Proposal
note_type: article
area: computer-science
domain: programming-languages
section: compilation
parent: "[[Program Binary Formats]]"
status: draft
related:
  - "[[Compilation]]"
  - "[[Executable Binary]]"
  - "[[Program Binary Formats]]"
  - "[[ELF]]"
  - "[[DWARF]]"
  - "[[Linking]]"
tags: []
---

# Program Binary Formats Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для темы `Program Binary Formats`, в которую естественно помещается рассмотрение таких понятий, как `ELF` и `DWARF`, по правилам `Principia Rerum`.

Для этой ветки достаточно уже существующей словарной рамки:

- `area: computer-science`
- `domain: programming-languages`
- `section: compilation`

Новый `domain` или отдельный `section` не нужен: речь идет не о новой дисциплине, а о локальном кластере внутри compilation-ветки.

## Рекомендуемая иерархия

```text
Compilation
└── Program Binary Formats
    ├── ELF
    └── DWARF
```

## Почему структура именно такая

- `Program Binary Formats` лучше сделать `overview`, потому что `ELF` и `DWARF` уже образуют локальный кластер про стандартизованные бинарные представления программного артефакта и его отладочных данных.
- `ELF` не стоит подвешивать напрямую под `Executable Binary`, потому что `Executable Binary` по текущей модели остается обычной `article`, а `parent` по правилам `Principia Rerum` должен указывать на обзорный узел.
- `DWARF` не стоит делать дочерней статьей строго только у `ELF`: на практике он часто встречается рядом с ELF, но понятийно описывает формат debug information, а не один конкретный executable container.
- `Executable Binary` лучше сохранить как общую статью про итоговый артефакт программы, а форматы вынести в отдельный локальный кластер.

## Что не стоит создавать заранее

- отдельный `domain` вроде `toolchain-formats`, потому что это слишком крупное решение ради локальной подветки;
- отдельный `overview` вроде `ELF Internals`, пока устройство ELF можно удерживать разделами внутри одной статьи;
- специальные template-файлы под binary-format notes, потому что по `Principia Rerum` здесь должны оставаться только канонические `Overview Template` и `Article Template`.

## Текущая физическая раскладка в Inbox

```text
01. Inbox/To Classify/Programming Languages/Compilation/Program Binary Formats/
├── Program Binary Formats.md
├── Program Binary Formats Structure Proposal.md
├── ELF.md
└── DWARF.md
```

## Предлагаемое физическое размещение после нормализации

После нормализации в `02. Corpus Mundi` эти заметки должны раскладываться по алфавитному индексному написанию, а логическая ветка должна удерживаться через `parent`.

## Созданные seed-заготовки

- `[[Program Binary Formats]]`
- `[[ELF]]`
- `[[DWARF]]`

## Следующий шаг перед переносом в Corpus Mundi

1. Уточнить границу между `Executable Binary` как общим артефактом и `Program Binary Formats` как кластером конкретных представлений.
2. Проверить, когда рядом с `ELF` действительно нужны `PE` и `Mach-O`.
3. Проверить, когда рядом с `DWARF` действительно нужен более общий узел про debug information.
