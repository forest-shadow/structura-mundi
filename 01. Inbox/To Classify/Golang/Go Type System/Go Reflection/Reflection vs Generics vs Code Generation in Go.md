---
aliases:
  - Go Reflection vs Generics vs Code Generation
note_type: article
area: computer-science
domain: programming-languages
section: go
parent: "[[Go Reflection]]"
status: seed
related:
  - "[[Go Reflection]]"
  - "[[Go Type Parameters and Constraints]]"
  - "[[Reflection and Dynamic Decoding in Go]]"
  - "[[Performance and Limits of Go Reflection]]"
tags: []
---

# Reflection vs Generics vs Code Generation in Go

## Краткое определение

Статья о том, как в Go соотносятся reflection, generics и code generation как три разных способа работы с абстракцией, повторным использованием логики и динамической адаптацией данных.

## Основная идея или механизм

Эти подходы решают частично пересекающиеся задачи, но делают это на разных слоях: reflection переносит часть решений в runtime, generics сохраняют типовую информацию в compile-time-модели, а code generation выносит универсальность в стадию генерации кода.

## Границы темы

- В тему входят критерии выбора между reflection, generics и code generation, а также их различия по типобезопасности, производительности и прозрачности кода.
- На границе находятся детали API reflection и общие вопросы производительности, которые лучше держать в соседних заметках.

## Связи с другими заметками

Родительская тема:

`[[Go Reflection]]`

Связанные заметки:

- `[[Go Type Parameters and Constraints]]`
- `[[Reflection and Dynamic Decoding in Go]]`
- `[[Performance and Limits of Go Reflection]]`

## Примеры, случаи или следствия

- Generics не отменяют потребность в reflection там, где тип реально неизвестен до runtime.
- Code generation часто выигрывает в инфраструктурных сценариях, где нужна скорость и типовая прозрачность без runtime-магии.

## Что стоит раскрыть дальше

- [ ] Уточнить, где reflection действительно необходима, а где только привычна
- [ ] Добавить инженерные критерии выбора подхода
- [ ] Проверить `related`
