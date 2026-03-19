---
aliases:
  - Machine in GMP Model
  - M in GMP Model
  - Go M
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Scheduler GMP Model]]"
status: draft
related:
  - "[[Go Scheduler GMP Model]]"
  - "[[Go Goroutines]]"
  - "[[Go Scheduler Processor]]"
  - "[[Go Netpoller]]"
tags: []
---

# Go Machine Thread

## Краткое определение

Статья о сущности `M` в модели `G-M-P`: системном потоке исполнения, через который runtime Go выполняет goroutines и взаимодействует с операционной системой.

## Основная идея или механизм

`Go Machine Thread` не является самой задачей и не задаёт степень параллелизма Go-кода. Он выступает носителем исполнения: именно на `M` выполняются машинные инструкции, системные вызовы и переходы между runnable-работой и блокировками.

## Границы темы

- В тему входит роль `M` как OS thread в модели планировщика Go.
- На границе находятся `G` как единица работы и `P` как логическое право на исполнение Go-кода.

## Связи с другими заметками

Родительская тема:

`[[Go Scheduler GMP Model]]`

Связанные заметки:

- `[[Go Goroutines]]`
- `[[Go Scheduler Processor]]`
- `[[Go Netpoller]]`

## Примеры, случаи или следствия

Тема полезна для объяснения того, почему блокирующий syscall или `cgo` может удерживать системный поток, но не обязан полностью останавливать прогресс всего рантайма.

## Что стоит раскрыть дальше

- [ ] Уточнить связь между `M`, blocking syscalls и parking/unparking
- [ ] Решить, нужна ли отдельная связь с `LockOSThread`
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
