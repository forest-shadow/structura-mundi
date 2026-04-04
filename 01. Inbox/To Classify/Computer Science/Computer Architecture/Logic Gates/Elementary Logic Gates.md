---
aliases:
  - Basic Logic Gates
note_type: overview
area: computer-science
domain: computer-architecture
section: logic-gates
parent: "[[Logic Gates]]"
status: seed
related:
  - "[[Boolean Logic]]"
  - "[[Truth Table]]"
  - "[[Primitive Logic Gates]]"
tags: []
---

# Elementary Logic Gates

## Краткое определение области

`Elementary Logic Gates` - это минимальный набор базовых логических элементов, через которые обычно вводят аппаратную реализацию булевых операций: `NOT`, `AND` и `OR`.

## Что входит в эту тему

- `[[NOT Gate]]`
- `[[AND Gate]]`
- `[[OR Gate]]`

## Как устроена ветка

- Эти gates удобно держать вместе, потому что они задают базовый словарь для чтения цифровых схем.
- На текущем этапе не нужно дробить ветку дальше на отдельные технические подаспекты вроде transistor-level implementation или timing behavior.
- Для таблиц истинности и чисто логических соответствий стоит опираться на поперечные связи с `[[Truth Table]]` и `[[Boolean Logic]]`.

## Рекомендуемый маршрут чтения

1. Начать с `[[NOT Gate]]` как с унарной операции инверсии.
2. Затем перейти к `[[AND Gate]]` и `[[OR Gate]]` как к базовым бинарным комбинациям.
3. После этого посмотреть `[[Primitive Logic Gates]]`, чтобы увидеть универсальные эквиваленты.

## Соседние overview-ветки

- `[[Logic Gates]]`
- `[[Primitive Logic Gates]]`

## Что стоит раскрыть дальше

- [ ] Добавить краткие truth table examples
- [ ] Проверить связь с соответствующими заметками по булевой логике
- [ ] Уточнить границу между elementary и derived gates
- [ ] Проверить `related`
