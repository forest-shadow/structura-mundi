---
aliases:
  - Netpoller
  - Golang Netpoller
  - Сетевой опросчик Go
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Scheduler]]"
status: draft
related:
  - "[[Go Scheduler]]"
  - "[[Go Concurrency Model]]"
  - "[[Go Goroutines]]"
  - "[[Go Scheduler Preemption]]"
tags: []
---

# Go Netpoller

## Краткое определение

Статья о `netpoller` как части runtime Go, которая связывает неблокирующий ввод-вывод с пробуждением горутин и возвратом их в очередь исполнения scheduler.

## Основная идея или механизм

`Go Netpoller` позволяет рантайму ждать сетевые события через системные механизмы вроде `epoll`, `kqueue` или `IOCP`, не выделяя отдельный OS thread на каждое соединение. Когда событие готовности наступает, соответствующая goroutine переводится из ожидания обратно в runnable-состояние.

## Границы темы

- В тему входит связь между сетевым I/O, парковкой goroutines и повторным входом в scheduler.
- На границе находятся более общие вопросы concurrency model и более широкая тема системных вызовов в runtime Go.

## Связи с другими заметками

Родительская тема:

`[[Go Scheduler]]`

Связанные заметки:

- `[[Go Concurrency Model]]`
- `[[Go Goroutines]]`
- `[[Go Scheduler Preemption]]`

## Примеры, случаи или следствия

`Go Netpoller` объясняет, почему большое число сетевых соединений в Go обычно не требует по одному системному потоку на соединение и как I/O-нагрузка влияет на поведение scheduler.

## Что стоит раскрыть дальше

- [ ] Уточнить связь между netpoller и блокирующими syscall
- [ ] Добавить связь с runtime timers
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
