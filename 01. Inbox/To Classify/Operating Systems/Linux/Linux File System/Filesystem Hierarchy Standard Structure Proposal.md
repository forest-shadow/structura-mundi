---
aliases:
  - FHS Structure Proposal
  - Filesystem Hierarchy Standard Branch Structure Proposal
note_type: article
area: computer-science
domain: operating-systems
section: linux
parent: "[[Linux File System]]"
status: seed
related:
  - "[[Linux]]"
  - "[[Linux File System]]"
  - "[[Linux Distribution]]"
  - "[[File Systems]]"
tags: []
---

# Filesystem Hierarchy Standard Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для темы `Filesystem Hierarchy Standard`, в которую естественно помещается рассмотрение стандарта FHS по правилам `Principia Rerum`.

Для этой ветки подходит уже существующая словарная рамка:

- `area: computer-science`
- `domain: operating-systems`
- `section: linux`

Новый `domain` или `section` не нужен: FHS является стандартом layout-соглашений внутри Linux/Unix-like файлового пространства, а не самостоятельной дисциплинарной областью.

## Рекомендуемая иерархия

```text
Operating Systems
└── Linux
    └── Linux File System
        └── Filesystem Hierarchy Standard
```

## Почему структура именно такая

- `Filesystem Hierarchy Standard` лучше сделать обычной `article`, потому что это конкретный стандарт каталоговой иерархии, а не самостоятельная overview-ветка.
- Родителем лучше выбрать `[[Linux File System]]`, потому что FHS описывает соглашения о назначении каталогов в Linux/Unix-like filesystem layout, а не общую теорию файловых систем.
- `[[Linux Distribution]]` должен быть связан через `related`, потому что дистрибутивы практически воплощают или отклоняют FHS, но не являются родительской темой стандарта.
- `[[File Systems]]` остается поперечной связью: она объясняет OS-level abstraction, но FHS относится к Linux-specific namespace layout.
- Отдельный `overview` `Linux Filesystem Hierarchy` пока не нужен: текущий корпус естественно помещается в одну статью FHS и родительскую статью `Linux File System`.

## Что не стоит создавать заранее

- отдельные article-заметки для `/bin`, `/etc`, `/usr`, `/var`, `/home`, `/opt`, `/srv`, `/tmp` и других каталогов, пока нет самостоятельного корпуса для каждого пути;
- отдельный `overview` `Linux Filesystem Hierarchy`, если он будет дублировать `Linux File System` и `Filesystem Hierarchy Standard`;
- переносить FHS напрямую под `File Systems`, потому что это слишком общая OS-level рамка;
- специальные тематические template-файлы под FHS: по `Principia Rerum` в системе должны оставаться только канонические `Overview Template` и `Article Template`.

## Текущая физическая раскладка в Inbox

```text
01. Inbox/To Classify/Operating Systems/Linux/
├── Linux.md
├── Linux Structure Proposal.md
└── Linux File System/
    ├── Linux File System.md
    ├── Linux File System Structure Proposal.md
    ├── Filesystem Hierarchy Standard.md
    └── Filesystem Hierarchy Standard Structure Proposal.md
```

## Предлагаемое физическое размещение после нормализации

Если заметка будет доведена до канонического состояния, ее физическое размещение должно следовать алфавитному правилу:

```text
02. Corpus Mundi/
├── F/
│   └── Filesystem Hierarchy Standard.md
└── L/
    ├── Linux.md
    ├── Linux Distribution.md
    ├── Linux File System.md
    └── Linux Kernel.md
```

Логическая ветка при этом все равно собирается через `parent`, а не через физическое соседство файлов.

## Созданные seed-заготовки

- `[[Filesystem Hierarchy Standard]]`

## Следующий шаг перед переносом в Corpus Mundi

1. Наполнить `Filesystem Hierarchy Standard` описанием границ стандарта и его отношения к реальным дистрибутивам.
2. Уточнить, какие каталоги стоит раскрывать внутри статьи как разделы, а не отдельные заметки.
3. Проверить связь с `[[Linux Distribution]]`, потому что дистрибутивы могут следовать FHS не буквально.
4. После содержательного наполнения поднять статус заметки с `seed` до `draft`.
