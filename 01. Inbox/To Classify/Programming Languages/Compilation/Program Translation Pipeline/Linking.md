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
  - "[[Object File]]"
  - "[[Shared Library]]"
  - "[[Executable Binary]]"
  - "[[Machine Code]]"
tags: []
---

# Linking

## Краткое определение

`Linking` — это стадия, на которой отдельные скомпилированные единицы и внешние зависимости связываются в более цельный бинарный артефакт.

## Основная идея или механизм

Linking разрешает внешние ссылки между фрагментами программы, собирает нужные части в общий результат и превращает набор `[[Object File]]` и библиотечных зависимостей в более цельный бинарный артефакт, например `[[Executable Binary]]` или `[[Shared Library]]`.

## Границы темы

- Входит: связывание compiled units, external symbols и формирование итогового бинарного результата.
- Входит: работа с `[[Object File]]` как типичным входом и выпуск `[[Shared Library]]` или `[[Executable Binary]]` как типичным выходом.
- Не входит: runtime loading после запуска программы.

## Связи с другими заметками

Родительская тема:

`[[Program Translation Pipeline]]`

Связанные заметки:

- `[[Code Generation]]`
- `[[Object File]]`
- `[[Shared Library]]`
- `[[Executable Binary]]`
- `[[Machine Code]]`

## Примеры, случаи или следствия

Даже если отдельные модули уже получили machine-level form, программа все еще может быть неполной, пока linker не свяжет `[[Object File]]` между собой и с нужными библиотеками.

Результатом linking может быть не только `[[Executable Binary]]`, но и `[[Shared Library]]`, поэтому сам linking нельзя описывать как стадию, которая всегда заканчивается именно запускным файлом.

## Что стоит раскрыть дальше

- [ ] Уточнить различие static linking и dynamic linking
- [ ] Уточнить связь с symbol resolution
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
