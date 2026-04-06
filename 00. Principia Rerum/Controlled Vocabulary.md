# Controlled Vocabulary

## Назначение

Этот документ фиксирует управляемые значения для основных полей `frontmatter` и правила расширения словаря.

Главный принцип:

- сначала переиспользовать уже существующее значение;
- новое значение вводить только при устойчивой необходимости;
- не расширять словарь ради одной заметки или случайной формулировки;
- для контролируемо-открытых словарей опираться прежде всего на уже существующие таксономии в `02. Corpus Mundi`.

## Статус словарей

В системе используются два режима словаря:

- `закрытый словарь` — новые значения не добавляются без явного изменения правил;
- `контролируемо-открытый словарь` — новые значения допустимы, но только по правилам этого документа.

Текущий режим по полям:

- `note_type` — закрытый словарь;
- `status` — закрытый словарь;
- `area` — закрытый словарь;
- `domain` — контролируемо-открытый словарь;
- `section` — контролируемо-открытый словарь.

## `note_type`

Утвержденные значения:

- `overview`
- `article`

Правило:

- `overview` используется для обзорного узла, который собирает под собой тему или подветку;
- `article` используется для обычной энциклопедической статьи по термину, аспекту, механизму или сущности;
- новые типы заметок не вводятся без устойчивого паттерна и отдельного решения на уровне правил.

Статус словаря:

- закрытый.

## `status`

Утвержденные значения:

- `seed`
- `draft`
- `reviewed`
- `evergreen`

Правило:

- использовать только эти значения, пока не принято отдельное изменение стандарта;
- если заметка не вписывается идеально, выбирать ближайший по смыслу статус, а не придумывать новый.

Статус словаря:

- закрытый.

## `area`

Текущий утвержденный словарь:

- `anthropology`
- `biology`
- `computer-science`
- `philosophy`
- `history`
- `literature`
- `religion`
- `linguistics`

Правило:

- `area` должно обозначать крупный мир знания, а не локальную тему;
- новое `area` вводится только если в базе появляется самостоятельный корпус заметок, который неестественно втискивать в существующие области.

Статус словаря:

- закрытый на текущем этапе;
- новое `area` допустимо только как явное изменение словаря на уровне правил, а не как локальное решение внутри одной заметки.

## `domain`

`domain` задает главную дисциплинарную или профессиональную оптику заметки внутри `area`.

Статус словаря:

- контролируемо-открытый.

### Активная таксономия `domain`, подтвержденная `Corpus Mundi`

#### Внутри `computer-science`

- `algorithms`
- `databases`
- `distributed-systems`
- `frontend-engineering`
- `programming-languages`
- `software-architecture`

#### Внутри `philosophy`

- `logic`

#### Внутри `history`

- `military-history`

#### Внутри `anthropology`

- пока нет подтвержденных `domain` в `Corpus Mundi`

#### Внутри `biology`

- пока нет подтвержденных `domain` в `Corpus Mundi`

### Как читать этот список

- Это не просто примеры, а фактически подтвержденные таксоны, уже использованные в `02. Corpus Mundi`.
- При появлении новой заметки агент должен сначала пытаться встроить ее в один из этих `domain`.
- Значения, которые встречались раньше только как примеры, но не подтверждены корпусом, не должны автоматически считаться активной таксономией.

### Правило

- `domain` должен быть одиночным полем;
- `domain` задает главную оптику заметки, а не полный список всех дисциплин, которых она касается;
- `domain` может быть пустым только у `area-level root overview`, которая описывает всю `area` целиком;
- если тема междисциплинарна, дополнительные перспективы выражаются через `related`, дочерние статьи или общую `section`, но не через множественный `domain`.

### Когда вводить новый `domain`

Новый `domain` допустим только если одновременно выполняются условия:

- в рамках существующего `area` регулярно возникает заметная группа тем;
- эту группу неудобно и неестественно размещать в уже существующих `domain`;
- новый `domain` нужен не для одной заметки, а для устойчивой серии заметок;
- его можно четко отличить от соседних `domain`.

### Рабочая таксономия `domain`, утвержденная до переноса в `Corpus Mundi`

Эти значения уже разрешены для нормализации рабочих веток в `Inbox`, даже если соответствующая ветка еще не перенесена в `02. Corpus Mundi`.

#### Внутри `computer-science`

- `artificial-intelligence`
- `computer-architecture`
- `networking`
- `software-development`

#### Внутри `literature`

- `literary-studies`

#### Внутри `religion`

- `mythology`
- `religious-studies`

#### Внутри `anthropology`

- `ethnobiology`

#### Внутри `biology`

- `biochemistry`
- `developmental-biology`
- `evolutionary-biology`
- `nutrition`

## `section`

`section` — это локальный тематический кластер внутри `domain`.

Статус словаря:

- контролируемо-открытый.

### Активная таксономия `section`, подтвержденная `Corpus Mundi`

#### `computer-science -> algorithms`

- `automata-theory`

#### `computer-science -> databases`

- `transactions`

#### `computer-science -> distributed-systems`

- `event-driven-architecture`

#### `computer-science -> frontend-engineering`

- `react`
- `react-hooks`

Эти значения считаются подтвержденными и активными:

- `domain: frontend-engineering`
- `section: react`
- `section: react-hooks`

Они уже используются в `Corpus Mundi` и не должны дальше помечаться как "предлагаемые новые значения" в рабочих React-ветках.

#### `computer-science -> programming-languages`

- `compilation`
- `go`
- `javascript`

#### `computer-science -> distributed-systems`

- `service-reliability`
- `messaging-and-coordination-models`

#### `philosophy -> logic`

- `syllogistics`

#### `history -> military-history`

- `russian-military-history`

#### `anthropology -> ethnobiology`

- пока нет подтвержденных `section` в `Corpus Mundi`

#### `biology -> nutrition`

- пока нет подтвержденных `section` в `Corpus Mundi`

#### `biology -> biochemistry`

- пока нет подтвержденных `section` в `Corpus Mundi`

### Как читать этот список

- Это рабочая карта уже существующих тематических кластеров корпуса.
- Если новая заметка естественно попадает в одну из этих веток, нужно использовать уже существующий `section`.
- Новый `section` не должен вводиться только потому, что тема звучит чуть иначе стилистически.

### Правило

- `section` должно быть достаточно узким, чтобы собирать родственные заметки в один раздел;
- `section` не должно дублировать имя `domain`;
- `section` может быть пустым только у `area-level root overview` и у `domain-root overview`;
- не нужно вводить служебные значения вроде `*-core`, если заметка описывает весь `domain`, а не внутренний кластер;
- новое `section` вводится тогда, когда появляется не одна заметка, а реальный тематический кластер.

### Когда вводить новый `section`

Новое `section` оправдано, если:

- в теме уже есть или ожидается несколько взаимосвязанных заметок;
- тема требует собственного обзорного узла или отдельного представления в Bases;
- существующие `section` описывают ее плохо или слишком широко.

### Рабочая таксономия `section`, утвержденная до переноса в `Corpus Mundi`

Эти значения уже разрешены для нормализации рабочих веток в `Inbox`, даже если соответствующая ветка еще не перенесена в `02. Corpus Mundi`.

#### `computer-science -> artificial-intelligence`

- `ai-foundations`
- `applied-ai`
- `ai-agent-systems`
- `agent-protocols`
- `openai-codex`
- `ai-assisted-software-development`

#### `computer-science -> computer-architecture`

- `instruction-set-architecture`
- `logic-gates`
- `microarchitecture`

#### `computer-science -> networking`

- `network-topology`
- `network-performance`
- `network-protocols`
- `traffic-intermediation`
- `network-security`
- `internet`
- `dns`
- `network-models`
- `packet-switches`

#### `computer-science -> databases`

- `database-partitioning`
- `database-connections`
- `redis`

#### `computer-science -> software-architecture`

- `architecture-patterns`
- `dependency-management`
- `design-principles`
- `performance-modeling`

#### `computer-science -> software-development`

- `vim`

#### `anthropology -> ethnobiology`

- `ethnomycology`

#### `biology -> nutrition`

- `vitamins`

#### `biology -> biochemistry`

- `antioxidants`
- `metabolism`

#### `biology -> developmental-biology`

- `ontogenesis`

#### `biology -> evolutionary-biology`

- `phylogenesis`

#### `literature -> literary-studies`

- `russian-literature`
- `lyric-genres`

#### `religion -> mythology`

- `greek-mythology`

#### `religion -> religious-studies`

- `entheogenic-traditions`

## Правило расширения словаря

Агент должен действовать в таком порядке:

1. Проверить, нет ли уже подходящего значения в этом документе.
2. Проверить, нет ли подходящего значения среди уже реально используемых значений в `02. Corpus Mundi`.
3. Если подходящее значение есть, использовать его.
4. Если есть сомнение между двумя существующими значениями, выбрать более устойчивое и узкое по смыслу.
5. Новое значение предлагать только тогда, когда старые значения действительно не покрывают тему.

## Как агент должен действовать при сомнении

Если тема не ложится в словарь идеально, агент должен действовать в таком порядке:

1. Сначала проверить существующие значения в этом документе.
2. Затем проверить фактические значения, уже использованные в заметках `Corpus Mundi`.
3. Затем выбрать ближайшее устойчивое значение, если оно не искажает смысл.
4. Только после этого предлагать новое значение как расширение словаря.

Новое значение не должно появляться молча.

Если агент предлагает новое значение, он обязан явно указать:

- для какого поля оно предлагается;
- почему существующие значения не подходят;
- почему новое значение будет полезно не одной, а серии заметок.

## Что запрещено

- вводить новое значение ради стилистического варианта;
- дублировать одно и то же различными формулировками;
- использовать `section` как замену `area` или `domain`;
- использовать `domain` как список всех дисциплин, которых касается тема.


