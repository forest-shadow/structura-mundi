---
aliases:
  - TLS Session Establishment
note_type: article
area: computer-science
domain: networking
section: network-security
parent: "[[TLS]]"
status: seed
related:
  - "[[TLS]]"
  - "[[TLS Certificate Validation]]"
  - "[[Mutual TLS]]"
  - "[[HTTPS]]"
tags: []
---

# TLS Handshake

## Краткое определение

`TLS Handshake` — это статья о фазе установления TLS-соединения, в которой стороны согласуют криптографические параметры, подтверждают подлинность и выводят общий секрет для защищенной сессии.

## Основная идея или механизм

Handshake в TLS — это не просто старт соединения, а отдельный protocol-flow, который переводит незащищенный транспортный канал в состояние, пригодное для конфиденциального и аутентифицированного обмена.

## Границы темы

- В тему входят основные этапы согласования параметров, проверки сертификата и установления session keys.
- Рядом находятся `[[TLS Certificate Validation]]` и `[[Mutual TLS]]`, потому что они раскрывают отдельные аспекты доверия и аутентификации внутри handshake.

## Связи с другими заметками

Родительская тема:

`[[TLS]]`

Связанные заметки:

- `[[TLS Certificate Validation]]`
- `[[Mutual TLS]]`
- `[[HTTPS]]`

## Примеры, случаи или следствия

Понимание handshake помогает объяснить, почему TLS влияет на latency установления соединения и почему termination, resumption и offloading имеют заметный operational effect.

## Что стоит раскрыть дальше

- [ ] Уточнить различие между full handshake и resumed session
- [ ] Проверить `related`
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
