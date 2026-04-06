---
aliases:
  - Linux Structure Proposal
  - Структура ветки Linux
note_type: article
area: computer-science
domain: operating-systems
section: linux
parent: "[[Operating Systems]]"
status: draft
related:
  - "[[Operating Systems]]"
  - "[[Linux]]"
  - "[[Linux Kernel]]"
  - "[[Linux Distribution]]"
  - "[[Linux File System]]"
  - "[[Containerization]]"
tags: []
---

# Linux Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для темы `Linux`, в которую естественно помещается рассмотрение этого понятия по правилам `Principia Rerum`.

## Выбранная оптика

- `area: computer-science`
- `domain: operating-systems`
- `section: linux` (предлагаемое новое значение)

Почему так:

- `Linux` не стоит выносить в отдельный `domain`, потому что это не новая большая дисциплинарная оптика, а устойчивый кластер внутри уже существующей темы ОС;
- помещать `Linux` просто как одиночную статью прямо под `Operating Systems` неудобно, потому что рядом естественно возникают как минимум `Linux Kernel` и `Linux Distribution`, а позднее могут появиться `Linux Namespaces`, `cgroups`, `systemd`, `procfs` и другие родственные темы;
- отдельный `section: linux` позволяет собрать Linux-ветку как самостоятельный локальный кластер, не смешивая ее напрямую с общими заметками про процессы, память и файловые системы.

## Канонические имена

- section-level overview: `Linux`
- article: `Linux Kernel`
- article: `Linux Distribution`
- article: `Linux File System`

Форма `GNU/Linux` лучше хранить в `aliases`, а не как отдельную параллельную каноническую заметку, если речь идет о той же обзорной теме.

## Рекомендуемая иерархия

```text
Operating Systems
└── Linux
    ├── Linux Kernel
    ├── Linux Distribution
    └── Linux File System
```

## Почему структура именно такая

- `Linux` лучше сделать `overview`, потому что это уже не один частный механизм, а устойчивый узел, где требуется развести как минимум систему в широком практическом смысле, ядро и модель дистрибуции.
- `Linux Kernel` нужен отдельной `article`, потому что в строгом техническом смысле Linux прежде всего обозначает ядро, и эту границу важно явно удерживать.
- `Linux Distribution` нужен отдельной `article`, потому что в повседневной инженерной практике Linux почти всегда используется как имя семейства систем, поставляемых не как «голое ядро», а как сборки с user space, package management и init-системой.
- `Linux File System` разумнее держать отдельной `article`, а не прятать внутри общей заметки `File Systems`, потому что здесь появляется Linux-specific слой: directory hierarchy, mount points, virtual file systems и системные соглашения вокруг `/proc`, `/sys`, `/dev`, `/etc` и `/home`.
- Глубже идти пока не стоит: отдельные заметки `Linux Namespaces`, `cgroups`, `systemd`, `procfs` или `sysfs` лучше создавать только когда рядом действительно накопится корпус, а не ради симметрии.

## Что не стоит создавать заранее

- отдельную корневую ветку `Unix`, если рядом еще нет устойчивого sibling-корпуса про BSD, POSIX и Unix philosophy;
- параллельную каноническую заметку `GNU/Linux`, если она будет дублировать `Linux` с тем же объемом смысла;
- отдельный `sub-overview` вроде `Linux File Systems`, пока в ветке есть только одна Linux-specific filesystem-note;
- отдельные заметки `Linux Namespaces`, `cgroups`, `systemd`, `initramfs`, `procfs`, `sysfs` и `udev`, пока они не нужны реальному локальному корпусу;
- специальные тематические template-файлы под Linux-ветку, потому что по `Principia Rerum` здесь должны оставаться только канонические `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение после нормализации

```text
02. Corpus Mundi/
├── L/
│   ├── Linux.md
│   ├── Linux Kernel.md
│   ├── Linux Distribution.md
│   └── Linux File System.md
└── O/
    └── Operating Systems.md
```

Логическая ветка при этом собирается через `parent`, а не через вложенные директории.

## Созданные seed-заготовки

- `Linux.md`
- `Linux Kernel.md`
- `Linux Distribution.md`
- `Linux File System.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Подтвердить `section: linux`.
2. Уточнить, остается ли `Linux` каноническим обзорным именем, а `GNU/Linux` только alias-формой.
3. Решить, когда рядом с `Linux File System` действительно нужны `procfs`, `sysfs` и `Filesystem Hierarchy Standard` как отдельные статьи.
4. Решить, когда рядом с `Linux Kernel` действительно нужны `Linux Namespaces` и `cgroups` как отдельные статьи.
5. Проверить границу между Linux-веткой и уже существующей веткой `Containerization`.