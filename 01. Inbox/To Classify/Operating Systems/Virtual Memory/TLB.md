---
aliases:
  - Translation Lookaside Buffer
note_type: article
area: computer-science
domain: operating-systems
section: memory-management
parent: "[[Paging]]"
status: seed
related:
  - "[[Page Table]]"
  - "[[Page Fault]]"
  - "[[Virtual Address Space]]"
tags: []
---

# TLB

## Краткое определение

`TLB` — это быстрый кэш отображений виртуальных страниц в физические фреймы, который уменьшает стоимость повторного обращения к page table.

## Почему тема находится в ветке Paging

Эта заметка нужна как часть runtime-механики paging: TLB не заменяет page table, а ускоряет частый путь address translation.

## Основная идея или механизм

- при обращении к памяти процессор сначала пытается найти отображение в TLB;
- при попадании перевод адреса ускоряется;
- при промахе приходится обращаться к page table и, возможно, обновлять TLB.

## Границы темы

- Входит: роль TLB как translation cache.
- Не входит: полный микроархитектурный разбор всех реализаций, политик замещения и tagged-TLB деталей.

## Примеры, случаи или следствия

Эта заметка должна показать, почему virtual memory без TLB может быть корректной, но существенно более дорогой по времени доступа.

## Связи с другими заметками

Родительская тема:

`[[Paging]]`

Связанные заметки:

- `[[Page Table]]`
- `[[Page Fault]]`
- `[[Virtual Address Space]]`

## Что стоит раскрыть дальше

- [ ] Добавить различие между TLB hit и TLB miss
- [ ] Показать связь между TLB и page table walk
- [ ] Проверить `aliases`
- [ ] Проверить `related`
