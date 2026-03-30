---
aliases: []
note_type: article
area: computer-science
domain: operating-systems
section: processes-and-threads
parent: "[[CPU Scheduling]]"
status: seed
related:
  - "[[CPU Scheduling]]"
  - "[[Process]]"
  - "[[Thread]]"
tags: []
---

# Context Switch

## Краткое определение

`Context Switch` — это механизм, через который ОС сохраняет execution context одной runnable unit и восстанавливает context другой, чтобы передать ей CPU.

## Почему тема находится в ветке Processes and Threads

Эта заметка относится к execution model ОС, потому что context switch связывает решение планировщика с фактической сменой исполняемого процесса или потока.

## Основная идея или механизм

- scheduler определяет, кому должен быть выдан CPU;
- context switch реализует эту смену через сохранение и восстановление состояния исполнения;
- стоимость переключения влияет на эффективность многозадачности и perceived responsiveness системы.

## Границы темы

- Входит: context switch как OS-level mechanism между runnable execution units.
- Не входит: microarchitectural разбор pipeline flushes и всех hardware-specific деталей.

## Связи с другими заметками

Родительская тема:

`[[CPU Scheduling]]`

Связанные заметки:

- `[[Process]]`
- `[[Thread]]`
- `[[Process State Model]]`

## Примеры, случаи или следствия

- Частое переключение контекста может ухудшать throughput даже при корректном scheduling policy.
- Для thread switching и process switching идея одна, но ресурсная стоимость обычно различается.

## Что стоит раскрыть дальше

- [ ] Уточнить различие между process switch и thread switch
- [ ] Добавить связь с cache locality и scheduler overhead
- [ ] Проверить `related`
