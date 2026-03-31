---
aliases: []
note_type: article
area: computer-science
domain: networking
section: network-models
parent: "[[Network Interaction Models]]"
status: draft
related:
  - "[[Network Interaction Models]]"
  - "[[Peer-to-Peer Model]]"
tags: []
---

# Broadcast and Multicast Model

## Краткое определение

`Broadcast and Multicast Model` - это модель сетевого взаимодействия, в которой сообщение адресуется не одному конкретному получателю, а всем узлам сегмента или выбранной группе участников.

## Основная идея или механизм

В отличие от point-to-point обмена, здесь сетевая доставка ориентирована на fan-out к множеству адресатов, что меняет semantics адресации, доставки и нагрузки на сеть.

## Границы темы

- Эта тема относится к модели сетевого распространения сообщения, а не к distributed pub-sub semantics.
- На границе находится `[[Request-Reply Model]]`, где взаимодействие обычно адресно и парно.

## Связи с другими заметками

Родительская тема:

`[[Network Interaction Models]]`

Связанные заметки:

- `[[Peer-to-Peer Model]]`

## Примеры, случаи или следствия

Multicast useful там, где одно сообщение должно эффективно дойти до группы receivers без отдельной point-to-point отправки каждому узлу.
