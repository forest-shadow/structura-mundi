---
aliases:
  - mTLS
  - Mutual Transport Layer Security
note_type: article
area: computer-science
domain: networking
section: network-security
parent: "[[TLS]]"
status: seed
related:
  - "[[TLS]]"
  - "[[TLS Handshake]]"
  - "[[TLS Certificate Validation]]"
  - "[[Service Mesh]]"
tags: []
---

![[01. Inbox/To Classify/Networking/Network Security/TLS/_resources/31c0ef009dfa6682831e2213e1dc1d26_MD5.jpg]]

![[01. Inbox/To Classify/Networking/Network Security/TLS/_resources/df7eaaae6cd70ce284790f26d8c93a95_MD5.jpg]]
# Mutual TLS

## Краткое определение

`Mutual TLS` — это статья о режиме TLS, в котором аутентификация выполняется с обеих сторон соединения: и сервер, и клиент предъявляют свои сертификаты.

## Основная идея или механизм

Mutual TLS расширяет обычную server-authenticated модель TLS до двустороннего trust establishment. Это делает mTLS полезным там, где нужно подтверждать identity не только сервера, но и клиента или сервиса.

## Границы темы

- В тему входят client certificate authentication и двусторонняя trust model поверх TLS.
- Рядом находится `[[Service Mesh]]`, потому что mTLS часто используется как operational mechanism во внутреннем service-to-service communication.

## Связи с другими заметками

Родительская тема:

`[[TLS]]`

Связанные заметки:

- `[[TLS Handshake]]`
- `[[TLS Certificate Validation]]`
- `[[Service Mesh]]`

## Примеры, случаи или следствия

mTLS особенно полезен во внутренних сервисных сетях, где нужно не просто шифровать трафик, а явно аутентифицировать обе стороны соединения.

## Что стоит раскрыть дальше

- [ ] Уточнить границу между mTLS как protocol pattern и mTLS rollout в service mesh
- [ ] Проверить `related`
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
