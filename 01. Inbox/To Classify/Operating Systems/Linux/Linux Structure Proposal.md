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
  - "[[Filesystem Hierarchy Standard]]"
  - "[[Containerization]]"
tags: []
---

# Linux Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для темы `Linux`, в которую естественно помещается рассмотрение этого понятия по правилам `Principia Rerum`.

## Выбранная оптика

- `area: computer-science`
- `domain: operating-systems`
- `section: linux`

Почему так:

- `Linux` не стоит выносить в отдельный `domain`, потому что это не новая большая дисциплинарная оптика, а устойчивый кластер внутри уже существующей темы ОС;
- помещать `Linux` просто как одиночную статью прямо под `Operating Systems` неудобно, потому что рядом естественно возникают как минимум `Linux Kernel` и `Linux Distribution`, а позднее могут появиться `Linux Namespaces`, `cgroups`, `systemd`, `procfs` и другие родственные темы;
- `section: linux` уже оправдан как рабочее значение для OS-ветки и позволяет собрать Linux-кластер, не смешивая его напрямую с общими заметками про процессы, память и файловые системы.

## Канонические имена

- section-level overview: `Linux` 
- article: `Linux Kernel``Containerization` 
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
        └── Filesystem Hierarchy Standard
```

## Почему структура именно такая

- `Linux` лучше сделать `overview`, потому что это уже не один частный механизм, а устойчивый узел, где требуется развести как минимум систему в широком практическом смысле, ядро и модель дистрибуции.
- `Linux Kernel` нужен отдельной `article`, потому что в строгом техническом смысле Linux прежде всего обозначает ядро, и эту границу важно явно удерживать.
- `Linux Distribution` нужен отдельной `article`, потому что в повседневной инженерной практике Linux почти всегда используется как имя семейства систем, поставляемых не как «голое ядро», а как сборки с user space, package management и init-системой.
- `Linux File System` разумнее держать отдельной `article`, а не прятать внутри общей заметки `File Systems`, потому что здесь появляется Linux-specific слой: directory hierarchy, mount points, virtual file systems и системные соглашения вокруг `/proc`, `/sys`, `/dev`, `/etc` и `/home`.
- `Filesystem Hierarchy Standard` теперь оправдан как дочерняя `article` внутри `Linux File System`, потому что это конкретный стандарт layout-соглашений, а не вся Linux filesystem model.
- Глубже идти пока не стоит: отдельные заметки `Linux Namespaces`, `cgroups`, `systemd`, `procfs` или `sysfs` лучше создавать только когда рядом действительно накопится корпус, а не ради симметрии.

## Что не стоит создавать заранее

- отдельную корневую ветку `Unix`, если рядом еще нет устойчивого sibling-корпуса про BSD, POSIX и Unix philosophy;
- параллельную каноническую заметку `GNU/Linux`, если она будет дублировать `Linux` с тем же объемом смысла;
- отдельный `sub-overview` вроде `Linux File Systems`, если текущие filesystem-related статьи помещаются под `Linux File System`;
- отдельные заметки `Linux Namespaces`, `cgroups`, `systemd`, `initramfs`, `procfs`, `sysfs` и `udev`, пока они не нужны реальному локальному корпусу;
- отдельные заметки для каждого FHS-каталога, пока их можно раскрыть разделами внутри `Filesystem Hierarchy Standard`;
- специальные тематические template-файлы под Linux-ветку, потому что по `Principia Rerum` здесь должны оставаться только канонические `Overview Template` и `Article Template`.

## Какие рабочие заготовки уже есть

- `Linux.md` как section-level overview
- `Linux Kernel.md` как article
- `Linux Distribution.md` как article
- `Linux File System.md` как article
- `Filesystem Hierarchy Standard.md` как article

Эти seed-заметки уже играют роль рабочих заготовок внутри `Inbox`; отдельные Linux-specific template-файлы для них не нужны.

## Предлагаемое физическое размещение после нормализации

```text
02. Corpus Mundi/
├── L/
│   ├── Linux.md
│   ├── Linux Kernel.md
│   ├── Linux Distribution.md
│   └── Linux File System.md
├── F/
│   └── Filesystem Hierarchy Standard.md
└── O/
    └── Operating Systems.md
```

Логическая ветка при этом собирается через `parent`, а не через вложенные директории.

## Созданные seed-заготовки

- `Linux.md`
- `Linux Kernel.md`
- `Linux Distribution.md`
- `Linux File System.md`
- `Filesystem Hierarchy Standard.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Уточнить, остается ли `Linux` каноническим обзорным именем, а `GNU/Linux` только alias-формой.
2. Решить, когда рядом с `Linux File System` действительно нужны `procfs` и `sysfs` как отдельные статьи.
3. Решить, когда рядом с `Linux Kernel` действительно нужны `Linux Namespaces` и `cgroups` как отдельные статьи.
4. Проверить границу между Linux-веткой и уже существующей веткой `Containerization`.
