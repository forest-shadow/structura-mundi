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
```

## Почему структура именно такая

- `Linux File System` лучше держать как Linux-specific `article`, а не как новый `overview`, потому что тема уже самостоятельна, но пока не тянет на отдельный плотный кластер.
- Общая заметка `[[File Systems]]` должна удерживать OS-level abstraction про persistent storage, а не перегружаться Linux-specific layout и виртуальными файловыми системами.
- `Linux File System` естественно подчиняется `[[Linux]]`, потому что здесь важны именно Linux-specific directory hierarchy, mount points, VFS-практика и системные соглашения.
- Поперечная связь с `[[File Systems]]` должна идти через `related`, а не через второе родительство.

## Что не стоит создавать прямо сейчас

- Отдельный `sub-overview` вроде `Linux File Systems`, если рядом еще нет плотного набора sibling-статей.
- Отдельные заметки `procfs`, `sysfs`, `tmpfs`, `udev`, `Filesystem Hierarchy Standard` и `mount namespaces`, пока они не нужны реальному локальному корпусу.
- Специальные Linux-specific template-файлы: по `Principia Rerum` в системе должны оставаться только канонические `Overview Template` и `Article Template`.

## Что стоит раскрыть дальше

- [ ] Проверить, когда рядом нужны `procfs` и `sysfs` как отдельные статьи
- [ ] Проверить, когда `Filesystem Hierarchy Standard` перестает помещаться внутрь одной Linux-specific article
- [ ] Проверить `related`