---
aliases: []
note_type: article
area: computer-science
domain: programming-languages
section: compilation
parent: "[[Program Translation Pipeline]]"
status: seed
related:
  - "[[Intermediate Representation]]"
  - "[[Machine Code]]"
  - "[[Linking]]"
tags: []
---

# Code Generation

## Краткое определение

`Code Generation` — это стадия, на которой внутреннее представление программы преобразуется в низкоуровневый код, привязанный к целевой архитектуре или формату исполнения.

## Основная идея или механизм

На этой стадии compiler выбирает инструкции, схемы размещения данных и другие машинно-зависимые формы, подготавливая программу к дальнейшей сборке и запуску.

## Границы темы

- Входит: lowering из IR в target-specific code, связь с machine code.
- Не входит: исходный parsing и финальная упаковка исполнимого артефакта как файла.

## Связи с другими заметками

Родительская тема:

`[[Program Translation Pipeline]]`

Связанные заметки:

- `[[Intermediate Representation]]`
- `[[Machine Code]]`
- `[[Linking]]`

## Примеры, случаи или следствия

Один и тот же алгоритм после code generation для разных архитектур может порождать разные инструкции, соглашения о вызовах и способы адресации памяти.

## Что стоит раскрыть дальше

- [ ] Уточнить связь с optimization и register allocation
- [ ] Проверить отличие machine code и assembly output
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
