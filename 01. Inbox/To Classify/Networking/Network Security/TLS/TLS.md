---
aliases:
  - Transport Layer Security
note_type: overview
area: computer-science
domain: networking
section: network-security
parent: "[[Network Security]]"
status: seed
related:
  - "[[Network Security]]"
  - "[[TLS Handshake]]"
  - "[[TLS Certificate Validation]]"
  - "[[Mutual TLS]]"
  - "[[TLS Termination]]"
  - "[[HTTP]]"
tags: []
---

# TLS

## Краткое определение области

`TLS` — это обзорная заметка о протоколе Transport Layer Security как о механизме защищенного сетевого соединения, внутри которого естественно собираются handshake, certificate validation, mutual authentication и инфраструктурные deployment patterns вроде termination.

## Что входит в эту тему

- `[[TLS Handshake]]`
- `[[TLS Certificate Validation]]`
- `[[Mutual TLS]]`
- `[[TLS Termination]]`

## Как устроена ветка

- `TLS` служит protocol-overview узлом и не должен сам пытаться до конца раскрыть все этапы установления соединения, trust model и deployment patterns.
- `TLS Handshake` удерживает фазу установления защищенной сессии и согласования параметров.
- `TLS Certificate Validation` описывает, как строится доверие к удаленной стороне через certificate chain и policy checks.
- `Mutual TLS` фиксирует отдельный operational pattern, в котором аутентифицируется не только сервер, но и клиент.
- `TLS Termination` описывает инфраструктурный способ завершения TLS на промежуточном узле и остается cross-cutting темой на границе security и traffic intermediation.

## Рекомендуемый маршрут чтения

1. Начать с `[[TLS Handshake]]`.
2. Затем перейти к `[[TLS Certificate Validation]]`.
3. После этого читать `[[Mutual TLS]]`.
4. Завершить `[[TLS Termination]]` как deployment-level аспектом TLS.

## Соседние overview-ветки

- Родительская рамка: `[[Network Security]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны отдельные notes про `TLS Versions` и `TLS Resumption`
- [ ] Проверить границу между `TLS` и `HTTPS`
- [ ] Проверить `related`
