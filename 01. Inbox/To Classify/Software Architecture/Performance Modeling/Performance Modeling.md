---
aliases: []
note_type: overview
area: computer-science
domain: software-architecture
section: performance-modeling
parent: "[[Software Architecture]]"
status: seed
related:
  - "[[Queuing Theory]]"
  - "[[Little's Law]]"
  - "[[Kendall Notation]]"
  - "[[Network Performance]]"
tags: []
---

# Performance Modeling

## Краткое определение области

`Performance Modeling` — это overview-узел для заметок о формальных моделях нагрузки и поведения систем под конкурирующим потоком запросов.

## Что входит в эту тему

- `[[Queuing Theory]]`
- `[[Little's Law]]`
- `[[Kendall Notation]]`

## Как устроена ветка

- `Performance Modeling` собирает не operational tuning и не набор метрик сам по себе, а именно математические рамки, через которые объясняются задержка, пропускная способность, concurrency и saturation.
- `Queuing Theory` здесь выступает общей теоретической статьей.
- `Little's Law` и `Kendall Notation` лучше держать рядом как самостоятельные формальные инструменты, а не как мелкие подпункты внутри одной страницы.
- Сетевая перспектива живет рядом через `[[Network Performance]]`, но не поглощает всю ветку.

## Рекомендуемый маршрут чтения

1. Начать с `[[Queuing Theory]]`.
2. Затем перейти к `[[Little's Law]]` как к базовой связи между ключевыми величинами.
3. После этого читать `[[Kendall Notation]]` для более строгого описания классов систем обслуживания.

## Соседние overview-ветки

- `[[Software Architecture]]`
- `[[Network Performance]]`

## Что стоит раскрыть дальше

- [ ] Проверить, когда рядом нужен отдельный узел для utilization и saturation
- [ ] Проверить, когда рядом нужен отдельный узел для queue disciplines
- [ ] Проверить `related`
