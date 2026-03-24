---
aliases:
  - Syscalls
note_type: article
area: computer-science
domain: operating-systems
section: system-calls
parent: "[[Operating Systems]]"
status: seed
related:
  - "[[Processes and Threads]]"
  - "[[File Systems]]"
tags: []
---

# System Calls

## Краткое определение

`System Calls` — это программный интерфейс, через который пользовательские программы обращаются к сервисам операционной системы.

## Почему тема находится в ветке Operating Systems

Эта заметка относится к корневой OS-ветке, потому что system calls образуют общий boundary between user code and kernel services, а не подмеханику только процессов, памяти или файловых систем.

## Основная идея или механизм

- программа в user space не выполняет privileged operations напрямую;
- она обращается к ОС через формализованный интерфейс вызовов;
- ядро принимает управление и выполняет нужную операцию от имени программы.

## Границы темы

- Входит: system call как boundary mechanism.
- Не входит: полный ABI-level разбор, interrupts, traps и API конкретных ОС.

## Примеры, случаи или следствия

Эта заметка должна показать, почему работа с файлами, памятью и процессами в прикладной программе в конечном счете проходит через controlled interface к ядру.

## Связи с другими заметками

Родительская тема:

`[[Operating Systems]]`

Связанные заметки:

- `[[Processes and Threads]]`
- `[[File Systems]]`

## Что стоит раскрыть дальше

- [ ] Уточнить связь между syscall interface и user/kernel boundary
- [ ] Добавить примеры типичных классов system calls
- [ ] Проверить `aliases`
- [ ] Проверить `related`
