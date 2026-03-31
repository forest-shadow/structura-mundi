---
aliases: []
note_type: article
area: computer-science
domain: programming-languages
section: compilation
parent: "[[Program Translation Pipeline]]"
status: seed
related:
  - "[[Code Generation]]"
  - "[[Executable Binary]]"
  - "[[Machine Code]]"
tags: []
---

# Linking

## Краткое определение

`Linking` — это стадия, на которой отдельные скомпилированные единицы и внешние зависимости связываются в более цельный исполнимый артефакт.

## Основная идея или механизм

Linking разрешает внешние ссылки между фрагментами программы, собирает нужные части в общий результат и приближает machine-level output к executable binary.

## Границы темы

- Входит: связывание compiled units, external symbols и формирование итогового исполнимого результата.
- Не входит: runtime loading после запуска программы.

## Связи с другими заметками

Родительская тема:

`[[Program Translation Pipeline]]`

Связанные заметки:

- `[[Code Generation]]`
- `[[Executable Binary]]`
- `[[Machine Code]]`

## Примеры, случаи или следствия

Даже если отдельные модули уже получили machine-level form, программа все еще может быть неполной, пока linker не свяжет их между собой и с нужными библиотеками.

## Что стоит раскрыть дальше

- [ ] Уточнить различие static linking и dynamic linking
- [ ] Проверить связь с object files и symbol resolution
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
