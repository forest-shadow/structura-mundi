---
aliases:
  - QUIC Branch Structure Proposal
  - Структура ветки QUIC
note_type: article
area: computer-science
domain: networking
section: network-protocols
parent: "[[Transport Layer Protocols]]"
status: draft
related:
  - "[[Network Protocols]]"
  - "[[Transport Layer Protocols]]"
  - "[[QUIC]]"
  - "[[HTTP Versions]]"
  - "[[TLS]]"
tags: []
---

# QUIC Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для темы `QUIC` внутри `Transport Layer Protocols` по правилам `Principia Rerum`.

Для этой темы не требуется новый `section`:

- `area: computer-science`
- `domain: networking`
- `section: network-protocols` (переиспользуем существующее значение)

## Рекомендуемая иерархия

```text
Networking
└── Network Protocols
    └── Transport Layer Protocols
        └── QUIC
```

Переиспользуемые соседние заметки:

- `HTTP Versions`
- `TLS`
- `TCP IP Transport Layer`

## Почему структура именно такая

- `QUIC` лучше оформлять как `article` внутри `Transport Layer Protocols`, потому что по своей смысловой роли это transport-level protocol, задающий модель соединения, multiplexing, recovery и congestion behavior.
- Тему не стоит подчинять `HTTP`, потому что `HTTP/3` является прикладным протоколом поверх QUIC, а не наоборот.
- Тему не стоит подчинять `TLS`, хотя QUIC и интегрирует handshake semantics TLS 1.3, потому что это не просто security-extension, а самостоятельный транспортный протокол.
- Отдельный `overview` для `QUIC` пока преждевременен: для него еще нет плотного корпуса дочерних заметок вроде `QUIC Streams`, `QUIC Connection Migration`, `QUIC Loss Recovery` или `QUIC Handshake`.
- При этом `QUIC` уже стоит вынести раньше `TCP` и `UDP`, потому что он нужен как отдельная каноническая точка пересечения transport semantics, modern web delivery и связи с `HTTP/3`.

## Что не нужно создавать заранее

Пока не стоит заводить отдельные узлы:

- `HTTP/3 over QUIC` как дочерний `overview` внутри transport-ветки;
- `QUIC Streams`, `QUIC Handshake`, `QUIC Congestion Control` и `QUIC Connection Migration` как отдельные статьи без соседнего корпуса;
- vendor-specific заметки вроде `gQUIC`, `Cloudflare QUIC` или `MsQuic`;
- отдельные template-файлы под transport protocols, потому что по `Principia Rerum` здесь достаточно канонических `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение после нормализации

Если заметка дойдет до канонического состояния, её физическое размещение должно следовать алфавитному правилу:

```text
02. Corpus Mundi/
└── Q/
    └── QUIC.md
```

Локальные вложения при необходимости:

```text
02. Corpus Mundi/Q/_resources/QUIC/
```

## Созданные черновые заметки

- `QUIC.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Проверить границу между `QUIC` как transport-level protocol и `HTTP/3` как application-level protocol.
2. Проверить границу между `QUIC` и `TLS`, особенно в части handshake reuse и отказа от классического TLS record layer.
3. Решить, когда внутри transport-ветки рядом нужны `TCP` и `UDP`.
4. После этого перевести заметку из `seed` в рабочий черновик и наполнить содержанием.
