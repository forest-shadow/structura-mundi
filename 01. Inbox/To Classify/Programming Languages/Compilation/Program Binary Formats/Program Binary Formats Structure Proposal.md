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
  - "[[Object File]]"
  - "[[Shared Library]]"
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
- `PE` и `Mach-O` не нужно добавлять в эту ветку автоматически только потому, что рядом уже есть `ELF`. По правилам `Principia Rerum` новый дочерний узел оправдан тогда, когда он уже нужен как самостоятельная каноническая точка чтения, а не просто как симметричный placeholder.
- `Object File` и `Shared Library` не стоит включать внутрь `Program Binary Formats`, потому что это не конкретные форматы, а типы бинарных артефактов. Их естественнее держать отдельными `article` рядом с `Executable Binary` на уровне `Compilation`.
- `DWARF` не стоит делать дочерней статьей строго только у `ELF`: на практике он часто встречается рядом с ELF, но понятийно описывает формат debug information, а не один конкретный executable container.
- Отдельный общий узел `Debugging Symbols` пока не нужен. Для текущего корпуса достаточно прояснить эту границу внутри `DWARF`; если позднее понадобится обобщающий материал, точнее будет каноническое имя `Debug Information`, а не более узкое `Debugging Symbols`.
- `Executable Binary` лучше сохранить как общую статью про итоговый артефакт программы, а форматы вынести в отдельный локальный кластер.

## Что не стоит создавать заранее

- отдельный `domain` вроде `toolchain-formats`, потому что это слишком крупное решение ради локальной подветки;
- `PE` и `Mach-O` как пустые симметричные заготовки без самостоятельного содержательного повода;
- общий узел `Debugging Symbols`, пока рядом с `DWARF` нет второго формата или отдельного корпуса про общую тему debug metadata;
- отдельный `overview` вроде `Binary Artifact Kinds` только ради того, чтобы формально собрать `Object File`, `Shared Library` и `Executable Binary`, если эти три статьи пока спокойно живут как плоские sibling-узлы под `Compilation`;
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

## Зафиксированные решения

1. Граница между `Executable Binary` и `Program Binary Formats` проходит по линии `артефакт` против `формата`: первая заметка описывает вид итогового результата сборки, вторая — конкретные стандартизованные представления бинарных файлов и debug metadata.
2. `PE` и `Mach-O` пока не нужны как обязательные siblings для `ELF`. Их стоит добавлять только при реальном расширении ветки в сторону межплатформенного сравнения контейнерных форматов.
3. `Object File` и `Shared Library` стоит держать отдельными `article` на уровне `Compilation`, а не детьми `Program Binary Formats`, потому что это виды артефактов, а не названия контейнерных стандартов.
4. Отдельный общий узел про `debugging symbols` пока не нужен. Текущую границу лучше удерживать внутри `DWARF`, прямо фиксируя, что DWARF шире, чем просто symbol names; если позднее появится общий узел, его лучше называть `Debug Information`.
