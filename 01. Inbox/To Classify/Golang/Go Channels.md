---
aliases:
  - Channels in Go
  - Каналы Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Concurrency Model]]"
status: draft
related:
  - "[[Go]]"
  - "[[Go Concurrency Model]]"
  - "[[Go Goroutines]]"
tags: []
---

# Go Channels

## Краткое определение

Статья о channels как основном механизме передачи значений и координации между goroutines в Go.

## Основная идея или механизм

Каналы в Go позволяют выражать communication and coordination через передачу данных, а не только через разделяемое состояние и блокировки.

## Границы темы

- В тему входят send/receive semantics, buffering и блокирующее поведение каналов.
- На границе находятся отдельные примитивы синхронизации и `select`.

## Связи с другими заметками

Родительская тема:

`[[Go Concurrency Model]]`

Связанные заметки:

- `[[Go Goroutines]]`
- `[[Go]]`

## Примеры, случаи или следствия

Канал может быть не просто транспортом значений, а способом описать саму структуру взаимодействия между concurrent routines.

## Что стоит раскрыть дальше

- [ ] Добавить buffered vs unbuffered channels
- [ ] Уточнить роль closing channels
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
