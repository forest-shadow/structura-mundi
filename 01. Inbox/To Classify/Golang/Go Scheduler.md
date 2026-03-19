---
aliases:
  - Golang Scheduler
  - Планировщик Go
note_type: overview
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Concurrency Model]]"
status: seed
related:
  - "[[Go Concurrency Model]]"
  - "[[Go Goroutines]]"
  - "[[Go Scheduler GMP Model]]"
  - "[[Go Scheduler Work Stealing]]"
  - "[[Go Scheduler Preemption]]"
tags: []
---

# Go Scheduler

## Краткое определение области

Обзорная заметка для планировщика Go как части runtime, отвечающей за исполнение goroutines, распределение работы и возврат управления между конкурентно исполняемыми задачами.

## Что входит в эту тему

- `[[Go Scheduler GMP Model]]`
- `[[Go Scheduler Work Stealing]]`
- `[[Go Scheduler Preemption]]`

## Как устроена ветка

- `Go Scheduler` является дочерним `overview` внутри `[[Go Concurrency Model]]`.
- Ветка остаётся минимальной и покрывает только самые устойчивые и полезные аспекты планировщика.
- Более глубокие внутренние детали рантайма стоит выносить только при появлении реального корпуса заметок.

## Рекомендуемый маршрут чтения

1. Начать с общей роли scheduler в runtime Go.
2. Затем перейти к `[[Go Scheduler GMP Model]]`.
3. После этого читать `[[Go Scheduler Work Stealing]]` и `[[Go Scheduler Preemption]]`.

## Соседние overview-ветки

- `[[Go Concurrency Model]]`

## Что стоит раскрыть дальше

- [ ] Уточнить границы между scheduler и goroutines
- [ ] Проверить, нужны ли отдельные статьи про sysmon и netpoller
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
