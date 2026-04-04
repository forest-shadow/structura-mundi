---
aliases: []
note_type: article
area: computer-science
domain: programming-languages
section: compilation
parent: "[[Compilation]]"
status: seed
related:
  - "[[Code Generation]]"
  - "[[Executable Binary]]"
  - "[[Program Translation Pipeline]]"
tags: []
---

# Machine Code

## Краткое определение

`Machine Code` — это набор низкоуровневых инструкций конкретной процессорной архитектуры, который может быть непосредственно интерпретирован аппаратным исполнителем CPU.

## Основная идея или механизм

В compilation-ветке machine code выступает как один из конечных результатов code generation и как переход от архитектурно-независимых представлений к архитектурно-зависимому исполнимому содержимому.

## Границы темы

- Входит: архитектурные инструкции, зависимость от ISA, роль machine code как результата трансляции.
- Не входит: формат исполнимого файла целиком и процесс загрузки программы в память.

## Связи с другими заметками

Родительская тема:

`[[Compilation]]`

Связанные заметки:

- `[[Code Generation]]`
- `[[Executable Binary]]`
- `[[Program Translation Pipeline]]`

## Примеры, случаи или следствия

Одинаковая high-level программа после трансляции в x86-64 и ARM machine code перестает быть одним и тем же двоичным текстом, хотя может сохранять одну и ту же семантику.

## Что стоит раскрыть дальше

- [ ] Уточнить отличие machine code от assembly
- [ ] Проверить связь с object files и executable formats
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
