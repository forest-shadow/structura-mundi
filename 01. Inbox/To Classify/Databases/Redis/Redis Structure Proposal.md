---
aliases:
  - Redis Structure Proposal
  - Структура ветки Redis
note_type: article
area: computer-science
domain: databases
section: redis
parent:
status: draft
related:
  - "[[Databases]]"
  - "[[Redis]]"
  - "[[Redis Sorted Set]]"
  - "[[Distributed Cache]]"
tags: []
---

# Redis Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для ветки `Redis`, в которую естественно помещается рассмотрение такого понятия, как `ZSET`, по правилам `Principia Rerum`.

## Выбранная оптика

- `area: computer-science`
- `domain: databases`
- `section: redis` (предлагаемое рабочее значение)

Почему так:

- `ZSET` в контексте Redis лучше понимать как Redis-специфичную структуру данных, а не как абстрактную caching-технику;
- существующий `domain: databases` уже покрывает тему естественнее, чем создание нового domain под один продукт;
- отдельный `section: redis` оправдан, потому что рядом с `ZSET` ожидается целая серия родственных заметок о типах данных и механизмах Redis.

## Канонические имена

- section-level overview: `Redis`
- article: `Redis Sorted Set`

Аббревиатуру `ZSET` лучше хранить в `aliases`, а не делать каноническим именем файла.

## Рекомендуемая иерархия

```text
Databases
└── Redis
    └── Redis Sorted Set
```

## Почему структура именно такая

- `Databases` уже существует как domain-root overview, поэтому новый верхний уровень создавать не нужно.
- `Redis` лучше сделать `overview`, потому что это не одиночный термин, а устойчивый кластер тем: data types, expiration, persistence, replication, pub/sub и operational behavior.
- `Redis Sorted Set` должен быть обычной `article`, потому что это один конкретный примитив внутри Redis, а не самостоятельная обзорная ветка.
- Дополнительный уровень `Redis Data Types` пока преждевременен: для одной заметки он только утяжелит дерево.

## Что не стоит делать прямо сейчас

- Не стоит помещать `ZSET` напрямую под `Databases`, потому что так теряется Redis-контекст.
- Не стоит относить `ZSET` только в `Caching`, потому что тогда пропадает product-specific data model perspective.
- Не стоит заводить отдельные заметки под каждый Redis command или command-family, пока не собран устойчивый корпус про сами структуры данных.
- Не стоит создавать специальные templates под Redis-ветку: по `Principia Rerum` здесь достаточно канонических `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
├── R/
│   ├── Redis.md
│   └── Redis Sorted Set.md
```

## Что уже создано в Inbox

- `[[Redis]]`
- `[[Redis Sorted Set]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом с `Redis Sorted Set` нужны другие Redis data type notes
- [ ] Решить, когда нужен промежуточный overview `Redis Data Types`, если ветка реально разрастется
- [ ] Подтвердить `section: redis`
- [ ] Проверить `related`
