---
aliases:
  - Linux Filesystem Structure Proposal
note_type: article
area: computer-science
domain: operating-systems
section: linux
parent: "[[Linux]]"
status: draft
related:
  - "[[Linux]]"
  - "[[Linux File System]]"
  - "[[Filesystem Hierarchy Standard]]"
  - "[[File Systems]]"
  - "[[Linux Kernel]]"
  - "[[Linux Distribution]]"
tags: []
---

# Linux File System Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для темы `Linux File System` внутри более общей ветки `Linux` по правилам `Principia Rerum`.

## Рекомендуемая иерархия

```text
Operating Systems
├── File Systems
└── Linux
    ├── Linux Kernel
    ├── Linux Distribution
    └── Linux File System
        └── Filesystem Hierarchy Standard
```

## Почему структура именно такая

- `Linux File System` лучше держать как Linux-specific `article`, а не как новый `overview`, потому что тема уже самостоятельна, но пока не тянет на отдельный плотный кластер.
- `Filesystem Hierarchy Standard` лучше держать дочерней `article` внутри `Linux File System`, потому что FHS описывает конкретный стандарт каталогового layout, а не всю файловую модель Linux.
- Общая заметка `[[File Systems]]` должна удерживать OS-level abstraction про persistent storage, а не перегружаться Linux-specific layout и виртуальными файловыми системами.
- `Linux File System` естественно подчиняется `[[Linux]]`, потому что здесь важны именно Linux-specific directory hierarchy, mount points, VFS-практика и системные соглашения.
- `Filesystem Hierarchy Standard` полезно связать с `[[Linux Distribution]]` через `related`, потому что дистрибутивы воплощают FHS в конкретной системной политике.
- Поперечная связь с `[[File Systems]]` должна идти через `related`, а не через второе родительство.

## Какие рабочие заготовки уже есть

- `Linux File System.md` как seed-статья для канонического термина
- `Linux File System Structure Proposal.md` как правило раскладки ветки в `Inbox`
- `Filesystem Hierarchy Standard.md` как seed-статья про FHS
- `Filesystem Hierarchy Standard Structure Proposal.md` как правило раскладки FHS-узла

Отдельный Linux-specific template-файл для этой темы не нужен: по `Principia Rerum` содержательные различия должны жить в самих seed-заметках и их `frontmatter`, а не в дополнительных шаблонах.

## Что не стоит создавать прямо сейчас

- Отдельный `sub-overview` вроде `Linux File Systems`, если рядом еще нет плотного набора sibling-статей.
- Отдельные заметки `procfs`, `sysfs`, `tmpfs`, `udev` и `mount namespaces`, пока они не нужны реальному локальному корпусу.
- Отдельные заметки для каждого FHS-каталога, пока достаточно раскрыть их разделами внутри `[[Filesystem Hierarchy Standard]]`.
- Специальные Linux-specific template-файлы: по `Principia Rerum` в системе должны оставаться только канонические `Overview Template` и `Article Template`.

## Что стоит раскрыть дальше

- [ ] Проверить, когда рядом нужны `procfs` и `sysfs` как отдельные статьи
- [ ] Наполнить `Filesystem Hierarchy Standard` таблицей ключевых каталогов
- [ ] Проверить `related`
