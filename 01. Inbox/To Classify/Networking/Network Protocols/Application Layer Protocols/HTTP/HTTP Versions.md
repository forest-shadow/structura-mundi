---
aliases: []
note_type: article
area: computer-science
domain: networking
section: network-protocols
parent: "[[HTTP]]"
status: seed
related:
  - "[[HTTP]]"
  - "[[HTTP Messages]]"
  - "[[TCP IP Transport Layer]]"
tags: []
---

# HTTP Versions

## Краткое определение

`HTTP Versions` — это статья о развитии HTTP от ранних текстовых версий к современным вариантам с иным framing и transport behavior.

## Границы темы

- Входит: общая линия различий между HTTP/1.1, HTTP/2 и HTTP/3.
- Не входит: низкоуровневый детальный разбор всех frame formats и transport internals.

## Связи с другими заметками

Родительская тема:

`[[HTTP]]`

Связанные заметки:

- `[[HTTP Messages]]`
- `[[TCP IP Transport Layer]]`

## Примеры, случаи или следствия

- Эволюция версий показывает, что semantics HTTP в значительной степени стабильны, даже когда transport and framing model меняются.
- Различия между версиями важны для производительности, multiplexing и connection behavior.

## Что стоит раскрыть дальше

- [ ] Проверить, когда нужен отдельный раздел про HTTP/2 multiplexing и HTTP/3 over QUIC
- [ ] Проверить `related`
