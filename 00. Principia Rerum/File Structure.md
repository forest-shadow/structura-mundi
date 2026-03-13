# Базовая идея

> Структура Vault **максимально плоская и функциональная**: **папки должны отражать не предметную классификацию, а роль файла в системе.**  Предметная классификация уже живёт в `frontmatter` и Bases.

- **служебные документы отдельно**;
- **канонические энциклопедические статьи отдельно**;
- **учебные маршруты и карты отдельно**;
- **общие и тяжёлые вложения отдельно**;
- **черновой импорт отдельно**.

# Рекомендуемая структура vault

Пример рекомендуемой структуры:

```text
Structura Mundi/
├── Tabula Ortus.md                     # Enter point for Structura Mundi vault
├── 00. Principia Rerum/                # Principia Rerum — Knowledge system rules
│   ├── Knowledge Base Standard.md
│   ├── Knowledge System Model.md
│   ├── Frontmatter Legend.md
│   ├── Controlled Vocabulary.md
│   ├── Tag Policy.md
│   ├── Naming Policy.md
│   ├── Note Lifecycle and Merge Policy.md
│   └── Templates/
│       ├── Overview Template.md
│       └── Article Template.md
│
├── 00. Obsidian Praxis/                # Obsidian practice, templates and setup notes
│   ├── __00. Obsidian Praxis.md
│   ├── Git History Squash.md
│   ├── Templates/
│   │   ├── Overview Template.md
│   │   └── Article Template.md
│   └── Config & Settings Details/
│
├── 01. Inbox/
│   ├── To Classify/
│   ├── To Rewrite/
│   └── To Merge/
│
├── 02. Corpus Mundi/
│   ├── A/
│   ├── B/
│   ├── C/
│   ├── D/
│   ├── O/
│   │   ├── OLTP.md
│   │   └── _resources/
│   │       └── OLTP/
│   │           └── transaction-flow.png
│   ├── ...
│   └── Z/
│
├── 03. Maps and Courses/
│   ├── Topic Maps/
│   ├── Learning Paths/
│   └── Reading Orders/
│
├── 04. Assets/
│   ├── Shared/
│   │   ├── Images/
│   │   └── Diagrams/
│   └── Imported/
│       └── PDFs/
│
└── 99. Archive/
    ├── Deprecated/
    ├── Merged/
    └── Old Structures/
```

## Что должно лежать в каждой папке

## `00. Principia Rerum/`

Это “конституция” базы.

Там должны лежать не знания по предметам, а правила самой системы:
- `Knowledge Base Standard.md` — правила ведения базы;
- `Knowledge System Model.md` — объясняющая модель того, как устроена система знаний;
- `Frontmatter Legend.md` — назначение каждого поля;
- `Controlled Vocabulary.md` — допустимые значения `area`, `domain`, `status`;
- `Tag Policy.md` — какие теги разрешены и для чего;
- `Naming Policy.md` — как называть заметки и связанные файлы;
- `Note Lifecycle and Merge Policy.md` — как создавать, сливать, переименовывать и архивировать заметки;
- `Templates/` — расширенные шаблоны для агента.

Эта папка нужна, чтобы база не расползалась.

## `00. Obsidian Praxis/`

Это отдельный инструментальный раздел.

Там должны лежать не правила архитектуры базы знаний, а практические материалы по работе с Obsidian:
- Obsidian-шаблоны;
- Markdown- и editor-specific заметки;
- заметки по настройкам и конфигурации;
- рабочие приемы, связанные именно с Obsidian.

Например:
- `Templates/` — минимальные шаблоны для стандартного механизма шаблонов Obsidian;
- `Config & Settings Details/` — заметки по настройкам и практикам;
- `Git History Squash.md` — отдельный инструментальный workflow note.


## `01. Inbox/`

Это буфер между хаосом и энциклопедией.

Сюда попадает всё, что ещё не стало канонической статьёй:
- импортированные черновики;
- наметки из других vault;
- заметки, которые ещё не классифицированы;
- куски, которые надо слить с существующими статьями.

Очень полезная папка, потому что она не позволяет засорять `02. Corpus Mundi/` сырыми материалами.

## `02. Corpus Mundi/`

Это ядро всей системы.

Сюда идут **все канонические энциклопедические статьи**, и обзорные, и обычные.

Здесь я бы оставил строго алфавитную структуру:

```text
02. Corpus Mundi/
├── O/
│   ├── OLTP.md
│   ├── OLTP Databases.md
│   ├── OLTP workload.md
│   └── OLTP systems.md
│
├── L/
│   ├── Load Balancing.md
│   ├── Load Balancing Algorithms.md
│   ├── Load Balancer Types.md
│   └── Layer 7 Load Balancing.md
│
├── H/
│   └── Health Checks.md
│
└── S/
    └── Session Affinity.md
```

## `03. Maps and Courses/`

Это не энциклопедические статьи, а **навигационные и учебные конструкции**.

Они вынесены отдельно, чтобы не смешивать:
- статью как единицу знания;
- маршрут чтения;
- карту темы;
- курс.

Например:

```text
03. Maps and Courses/
├── Topic Maps/
│   ├── OLTP Map.md
│   ├── Load Balancing Map.md
│   └── Caching Map.md
│
├── Learning Paths/
│   ├── OLTP Foundations.md
│   ├── System Design Fundamentals.md
│   └── Distributed Systems Core.md
│
└── Reading Orders/
    ├── Databases Reading Order.md
    └── Philosophy Reading Order.md
```

### Чем это отличается от `02. Corpus Mundi/`

- `02. Corpus Mundi/O/OLTP.md` — каноническая обзорная статья;
- `03. Maps and Courses/Topic Maps/OLTP Map.md` — карта навигации по теме;
- `03. Maps and Courses/Learning Paths/OLTP Foundations.md` — учебная последовательность.

Это три разные сущности.

## `04. Assets/`

Эта папка нужна, но **не как общий склад всех вложений подряд**.

Основное правило такое:
- ассеты, относящиеся к одной конкретной заметке, хранить локально рядом с ней;
- для этого использовать `_resources/` внутри алфавитной папки;
- внутри `_resources/` делать подпапки по заметкам;
- `04. Assets/` использовать только для общих и тяжёлых материалов.

То есть:

- `02. Corpus Mundi/O/_resources/OLTP/transaction-flow.png` — локальный ресурс заметки `OLTP`;
- `04. Assets/Shared/Diagrams/consistency-models.png` — общий ресурс, который используется во многих статьях;
- `04. Assets/Imported/PDFs/paper-name.pdf` — тяжёлый импортированный файл.

Почему так:
- заметка и её материалы находятся рядом;
- поиск проще, потому что ресурсы группируются по теме, а не сваливаются в один общий склад;
- алфавитная папка остаётся индексом, а не онтологией;
- общие файлы не дублируются по множеству локальных папок.

Пример локального хранения:

```text
02. Corpus Mundi/
└── O/
    ├── OLTP.md
    ├── OLTP Databases.md
    └── _resources/
        ├── OLTP/
        │   ├── transaction-flow.png
        │   └── architecture.svg
        └── OLTP Databases/
            └── engine-comparison.png
```

Пример общих и тяжёлых ассетов:

```text
04. Assets/
├── Shared/
│   ├── Images/
│   └── Diagrams/
└── Imported/
    └── PDFs/
```


## `99. Archive/`

Нужна для санитарии.

Сюда убираются:
- заметки, которые были слиты;
- старые версии;
- устаревшие структуры;
- черновики, потерявшие актуальность.

Очень важно не удалять всё сразу, но и не оставлять мусор в рабочем ядре.

# Где что хранить на практике

## Каноническая статья

Идёт в `02. Corpus Mundi/<Letter>/`.

Примеры:
- `OLTP.md`
- `OLTP Databases.md`
- `Causal Consistency.md`
- `Theism.md`

## Обзорная статья

Тоже идёт в `02. Corpus Mundi/<Letter>/`.

Пример:
- `Load Balancing.md`

Не нужно для неё отдельное физическое место.

## Учебный маршрут

Идёт в `03. Maps and Courses/Learning Paths/`.

Пример:
- `Load Balancing Foundations.md`

## Карта темы

Идёт в `03. Maps and Courses/Topic Maps/`.

Пример:
- `OLTP Map.md`

## Ассет конкретной статьи

Идёт в локальный `_resources/` рядом с заметкой.

Примеры:
- `02. Corpus Mundi/O/_resources/OLTP/transaction-flow.png`
- `02. Corpus Mundi/L/_resources/Load Balancing/layer-7.svg`

## Общий или тяжёлый ассет

Идёт в `04. Assets/Shared/` или `04. Assets/Imported/`.

Примеры:
- `04. Assets/Shared/Diagrams/consistency-models.png`
- `04. Assets/Imported/PDFs/paper-name.pdf`

## Сырой импорт из другого vault

Идёт в `01. Inbox/To Rewrite/` или `To Classify/`.


# Как я бы раскладывал ваши темы

## Пример: OLTP

```text
02. Corpus Mundi/O/
├── OLTP.md
├── OLTP Databases.md
├── OLTP workload.md
├── OLTP systems.md
└── _resources/
    └── OLTP/
        └── transaction-flow.png

03. Maps and Courses/Topic Maps/
└── OLTP Map.md

03. Maps and Courses/Learning Paths/
└── OLTP Foundations.md
```

## Пример: Load Balancing

```text
02. Corpus Mundi/L/
├── Load Balancing.md
├── Load Balancing Algorithms.md
├── Load Balancer Types.md
└── Load Balancing and High Availability.md

02. Corpus Mundi/R/
└── Round Robin.md

02. Corpus Mundi/H/
└── Health Checks.md

02. Corpus Mundi/S/
└── Session Affinity.md

03. Maps and Courses/Topic Maps/
└── Load Balancing Map.md
```

# Почему такая структура хороша

1. Структура не дублирует классификацию. 
	* Тематическая логика живёт в frontmatter и Bases.  Папки остаются скучными и устойчивыми.
	- Вы не строите одновременно:
		- папки по темам,
		- теги по темам,
		- поля по темам,
		- курсы по темам.
2. <b>Структура не смешивает типы сущностей</b>: у каждой сущности есть своё место.
	- Очень важно не смешивать:
		- статью;
		- карту темы;
		- курс;
		- сырой черновик;
		- служебный документ.
3. <b>Структура хорошо масштабируется</b>: Когда появится 500+ заметок, эта структура останется читаемой.
