---
aliases: []
note_type: overview
area: computer-science
domain: programming-languages
section: compilation
parent: "[[Compilation]]"
status: seed
related:
  - "[[Compilation]]"
  - "[[Executable Binary]]"
  - "[[Linking]]"
  - "[[ELF]]"
  - "[[DWARF]]"
tags: []
---

# Program Binary Formats

## Краткое определение области

`Program Binary Formats` - это локальный overview внутри `Compilation`, который собирает стандартизованные форматы представления бинарных программных артефактов и их отладочных метаданных.

## Что входит в эту тему

- `[[ELF]]`
- `[[DWARF]]`

## Как устроена ветка

- `Program Binary Formats` нужен как промежуточный `overview`, потому что `ELF` и `DWARF` не должны висеть прямо на общей статье `Compilation` без локального кластера.
- `ELF` остается обычной `article`, потому что это конкретный формат object files, shared objects и executable binaries.
- `DWARF` тоже остается обычной `article`, потому что это конкретный формат debug information, а не новый обзорный слой.
- `Executable Binary` лучше сохранять отдельной общей статьей про исполнимый артефакт как таковой, а не превращать ее в контейнер для всех форматов.

## Рекомендуемый маршрут чтения

1. Начать с `[[Compilation]]`.
2. Затем перейти к `[[Executable Binary]]`, чтобы зафиксировать сам артефакт.
3. После этого читать `[[Program Binary Formats]]`, `[[ELF]]` и `[[DWARF]]`, если нужен уровень конкретных бинарных представлений и debug metadata.

## Соседние overview-ветки

- `[[Compilation]]`
- `[[Program Translation Pipeline]]`

## Что стоит раскрыть дальше

- [ ] Проверить, когда рядом с `ELF` действительно нужны `PE` и `Mach-O`
- [ ] Проверить, нужен ли рядом отдельный узел про object files и shared libraries
- [ ] Проверить границу между `DWARF` и общей темой debugging symbols
- [ ] Проверить `related`
