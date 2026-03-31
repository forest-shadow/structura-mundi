---
aliases: []
note_type: article
area: computer-science
domain: distributed-systems
section: messaging-and-coordination-models
parent: "[[Messaging and Coordination Models]]"
status: draft
related:
  - "[[Messaging and Coordination Models]]"
  - "[[Coordination and Consensus]]"
tags: []
---

# Gossip Model

## Краткое определение

`Gossip Model` - это модель распространения информации в распределенной системе, при которой узлы постепенно обмениваются состоянием или сообщениями с другими узлами по эпидемическому принципу.

## Основная идея или механизм

Информация не передается строго централизованно и не требует единой точки координации: она расходится по системе через повторяющиеся локальные обмены между peers.

## Границы темы

- Это не то же самое, что `[[Peer-to-Peer Model]]`: peer symmetry здесь важна, но основной фокус на механике dissemination.
- Это не то же самое, что strict consensus protocols.

## Связи с другими заметками

Родительская тема:

`[[Messaging and Coordination Models]]`

Связанные заметки:

- `[[Coordination and Consensus]]`
- `[[Peer-to-Peer Model]]`

## Примеры, случаи или следствия

Gossip useful там, где системе нужно децентрализованно распространять membership, health state или lightweight updates без жесткого центра.
