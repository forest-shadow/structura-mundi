---
aliases:
  - Linux File System Branch Structure Proposal
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
  - "[[Filesystem Hierarchy Standard]]"
  - "[[Linking Files]]"
  - "[[Hard Link]]"
  - "[[Symbolic Link]]"
tags: []
---

# Linux File System Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для темы `Linux File System`, в которую естественно помещается рассмотрение Linux-specific файлового пространства по правилам `Principia Rerum`.

Для этой ветки подходит уже существующая словарная рамка:

- `area: computer-science`
- `domain: operating-systems`
- `section: linux`

Новый `domain` или отдельный `section` не нужен: речь идёт не о новой дисциплине, а о локальном Linux-кластере внутри OS-ветки.

## Рекомендуемая иерархия

```text
Operating Systems
└── Linux
    └── Linux File System
        ├── Inode
        ├── Filesystem Hierarchy Standard
        └── Linking Files
            ├── Hard Link
            └── Symbolic Link
```

## Почему структура именно такая

- `Linux File System` теперь лучше сделать `overview`, потому что под ним уже устойчиво собираются как минимум layout-тема `Filesystem Hierarchy Standard`, structural article `Inode` и link-тема `Linking Files`.
- `Inode` оправдан как обычная `article` прямо под `Linux File System`, потому что это не частный аспект только `Hard Link`, а более широкая Linux filesystem-сущность, через которую удобно объяснять различие между file object, directory entry и именем пути.
- `Filesystem Hierarchy Standard` остаётся обычной `article`, потому что это конкретный стандарт расположения каталогов, а не отдельный обзорный слой.
- `Linking Files` лучше сделать вложенным `overview`, потому что вопрос file linking в Linux естественно распадается на как минимум два разных механизма: `Hard Link` и `Symbolic Link`.
- `Hard Link` и `Symbolic Link` разумно оставить обычными `article`, потому что это конкретные механизмы с чёткими границами, а не самостоятельные подветки.
- Не стоит поднимать `Linking Files` сразу на уровень `Linux` или `Operating Systems`: в этой оптике тема связана именно с Linux filesystem namespace и практикой работы с именами файлов.

## Что не стоит создавать заранее

- отдельный `overview` вроде `Linux Links`, если он будет дублировать `Linking Files`;
- отдельные статьи про каждую утилиту (`ln`, `readlink`, `stat`) до накопления корпуса про пользовательские инструменты;
- отдельный `overview` вроде `Inode Model`, если уже созданная статья `Inode` пока покрывает нужную гранулярность;
- специальные тематические template-файлы под Linux filesystem branch, потому что по `Principia Rerum` в системе должны оставаться только канонические `Overview Template` и `Article Template`.

## Текущая физическая раскладка в Inbox

```text
01. Inbox/To Classify/Operating Systems/Linux/
├── Linux.md
├── Linux Structure Proposal.md
└── Linux File System/
    ├── Linux File System.md
    ├── Linux File System Structure Proposal.md
    ├── Inode.md
    ├── Filesystem Hierarchy Standard.md
    ├── Filesystem Hierarchy Standard Structure Proposal.md
    └── Linking Files/
        ├── Linking Files.md
        ├── Linking Files Structure Proposal.md
        ├── Hard Link.md
        └── Symbolic Link.md
```

## Предлагаемое физическое размещение после нормализации

После нормализации в `02. Corpus Mundi` эти заметки должны раскладываться по алфавитному индексному написанию, а не по физической логической вложенности. Логическая ветка при этом должна собираться через `parent`.

## Созданные seed-заготовки

- `[[Linux File System]]`
- `[[Inode]]`
- `[[Linking Files]]`
- `[[Hard Link]]`
- `[[Symbolic Link]]`

## Следующий шаг перед переносом в Corpus Mundi

1. Уточнить границу между `Linux File System` и общей OS-level статьёй `File Systems`.
2. Проверить, когда рядом с `Inode` действительно нужны `pathname resolution` и `dentry` как отдельные статьи.
3. Согласовать эту ветку с `[[Linux]]`, `[[Filesystem Hierarchy Standard]]` и `[[Linking Files]]`.
4. После содержательного наполнения поднять `Linux File System` с `seed` до `draft`.
