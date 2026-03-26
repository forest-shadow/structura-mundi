---
aliases:
  - System Design
note_type: overview
area: computer-science
domain: software-architecture
section:
parent: "[[Computer Science]]"
status: seed
related:
  - "[[Design Principles]]"
  - "[[Dependency Management]]"
  - "[[Clean Architecture]]"
  - "[[Distributed Systems]]"
tags: []
---

# Software Architecture

## Краткое определение области

`Software Architecture` — это доменная обзорная заметка для веток про архитектурные принципы, организацию зависимостей, форму сборки приложения и устойчивые архитектурные стили на уровне программной системы.

## Что входит в эту тему

- `[[Design Principles]]`
- `[[Dependency Management]]`
- `[[Clean Architecture]]`

## Как устроена ветка

- `Design Principles` собирает архитектурные и проектные принципы, которыми удобно пользоваться как рамкой для оценки решений;
- `Dependency Management` собирает практики организации зависимостей, wiring-а и сборки приложения;
- `Clean Architecture` стоит рядом как устойчивая архитектурная рамка, а не как замена всей ветке;
- `Distributed Systems` остается соседней доменной веткой, потому что описывает уже не общие архитектурные практики, а особый класс систем с собственными ограничениями.

## Рекомендуемый маршрут чтения

1. Начать с `[[Design Principles]]`.
2. Затем перейти к `[[Dependency Management]]`.
3. После этого читать `[[Clean Architecture]]`.
4. Затем уже связывать эти темы с прикладными ветками вроде `[[Distributed Systems]]`.

## Соседние overview-ветки

- Родительская рамка: `[[Computer Science]]`

## Что стоит раскрыть дальше

- [ ] Проверить, что domain-root overview остается без `section`
- [ ] Проверить границы между software architecture и distributed systems
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
