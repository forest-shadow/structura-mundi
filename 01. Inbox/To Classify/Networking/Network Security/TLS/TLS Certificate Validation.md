---
aliases:
  - TLS Trust Validation
  - Certificate Validation in TLS
note_type: article
area: computer-science
domain: networking
section: network-security
parent: "[[TLS]]"
status: seed
related:
  - "[[TLS]]"
  - "[[TLS Handshake]]"
  - "[[Mutual TLS]]"
  - "[[HTTPS]]"
tags: []
---
![[01. Inbox/To Classify/Networking/Network Security/TLS/_resources/b4676f83739414c91dbae0c895706bf7_MD5.jpg]]
# TLS Certificate Validation

## Краткое определение

`TLS Certificate Validation` — это статья о том, как в TLS строится доверие к удаленной стороне через проверку certificate chain, identity binding и policy constraints.

## Основная идея или механизм

TLS сам по себе не гарантирует, что удаленная сторона — именно тот субъект, за которого себя выдает. Эту задачу решает validation certificate chain, hostname matching и проверка доверенной цепочки подписи.

## Границы темы

- В тему входят certificate chain, доверенный корень, hostname verification и базовые policy checks.
- Рядом находится `[[TLS Handshake]]`, но handshake описывает процесс установления соединения в целом, а не только trust validation.

## Связи с другими заметками

Родительская тема:

`[[TLS]]`

Связанные заметки:

- `[[TLS Handshake]]`
- `[[Mutual TLS]]`
- `[[HTTPS]]`

## Примеры, случаи или следствия

Понимание certificate validation объясняет, почему self-signed certificates, expired certificates или hostname mismatch ломают доверие даже при формально работающем шифровании.

## Что стоит раскрыть дальше

- [ ] Уточнить роль certificate chain, hostname verification и trust store
- [ ] Проверить `related`
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
