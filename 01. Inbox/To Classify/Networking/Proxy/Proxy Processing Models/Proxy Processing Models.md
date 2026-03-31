---
aliases: []
note_type: overview
area: computer-science
domain: networking
section: traffic-intermediation
parent: "[[Proxy]]"
status: seed
related:
  - "[[Proxy]]"
  - "[[Circuit-Level Proxy]]"
  - "[[Application-Level Proxy]]"
  - "[[Layer 4 Proxy]]"
  - "[[Layer 7 Proxy]]"
tags: []
---

# Proxy Processing Models

## Краткое определение области

`Proxy Processing Models` — это обзорная заметка о том, на каком уровне и с какой глубиной прокси обрабатывает трафик.

## Что входит в эту тему

- `[[Circuit-Level Proxy]]`
- `[[Application-Level Proxy]]`
- `[[Layer 4 Proxy]]`
- `[[Layer 7 Proxy]]`

## Как устроена ветка

- `Circuit-Level Proxy` описывает посредничество на уровне соединения, а не прикладного содержимого.
- `Application-Level Proxy` фиксирует семантически более глубокую обработку прикладного протокола.
- `Layer 4 Proxy` и `Layer 7 Proxy` дают удобную operational-классификацию по уровню сетевого стека.

## Что стоит раскрыть дальше

- [ ] Проверить границы между `Application-Level Proxy` и `Layer 7 Proxy`
- [ ] Проверить границы между `Circuit-Level Proxy` и `Layer 4 Proxy`
- [ ] Проверить `related`
