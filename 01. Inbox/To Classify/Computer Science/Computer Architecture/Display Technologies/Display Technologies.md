---
aliases:
  - Display Tech
note_type: overview
area: computer-science
domain: computer-architecture
section: display-technologies
parent: "[[Computer Architecture]]"
status: seed
related:
  - "[[Computer Architecture]]"
  - "[[Liquid Crystal Display (LCD)]]"
tags: []
---

# Display Technologies

## Краткое определение области

`Display Technologies` — это обзорная заметка для аппаратных технологий визуального вывода, через которые вычислительная система превращает электрический сигнал в наблюдаемое изображение на экране или другой визуальной поверхности.

## Что входит в эту тему

- `[[Liquid Crystal Display]]`

## Как устроена ветка

- `Display Technologies` оформляется как отдельный `overview`, потому что темы вроде `Liquid Crystal Display`, `OLED`, `CRT` и `E Ink` образуют естественный технологический кластер и не должны висеть как несвязанные article-notes.
- `Liquid Crystal Display` пока уместно держать обычной `article`, потому что самой по себе LCD-теме еще не нужен собственный локальный overview-кластер.
- Поперечные связи с графическим стеком, GPU и human-computer-facing hardware лучше держать через `related`, а не через родительство внутри этой ранней ветки.

## Рекомендуемый маршрут чтения

1. Начать с `[[Display Technologies]]` как обзорного узла.
2. Затем перейти к `[[Liquid Crystal Display]]` как первой конкретной технологии в ветке.
3. После этого решать, нужны ли рядом отдельные заметки про `OLED`, `CRT` и другие display families.

## Соседние overview-ветки

- `[[Computer Architecture]]`

## Что стоит раскрыть дальше

- [ ] Проверить, когда рядом с `Liquid Crystal Display` нужны `OLED`, `CRT` и `E Ink`
- [ ] Уточнить границу между display hardware, graphics pipeline и user-interface темами
- [ ] Проверить `related`
