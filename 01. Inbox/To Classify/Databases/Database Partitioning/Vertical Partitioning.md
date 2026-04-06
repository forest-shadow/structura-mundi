---
aliases:
  - Vertical Database Partitioning
note_type: article
area: computer-science
domain: databases
section: database-partitioning
parent: "[[Database Partitioning]]"
status: seed
related:
  - "[[Horizontal Partitioning]]"
  - "[[Partitioning Strategy Selection]]"
  - "[[Partitioning Trade-offs]]"
tags: []
---

# Vertical Partitioning

## Краткое определение

`Vertical Partitioning` — это разбиение данных по колонкам, когда часто используемые и редко используемые атрибуты раскладываются по разным физическим структурам при сохранении общей логической сущности.

## Основная идея или механизм

Главная цель вертикального partitioning — сократить ширину горячих строк, уменьшить I/O и отделить часто читаемые или обновляемые поля от тяжелых, редко нужных или объемных колонок. Обычно такие части связываются общим идентификатором сущности.

## Границы темы

- Входит: hot/cold column split, вынос больших BLOB/TEXT-полей, разделение operational и archival attributes, уменьшение row width.
- Не входит: разбиение строк по ключу между partitions или узлами; это относится к `[[Horizontal Partitioning]]`.

## Связи с другими заметками

Родительская тема:

`[[Database Partitioning]]`

Связанные заметки:

- `[[Horizontal Partitioning]]`
- `[[Partitioning Strategy Selection]]`
- `[[Partitioning Trade-offs]]`

## Примеры, случаи или следствия

Вертикальное partitioning уместно, когда в одной широкой таблице есть небольшое горячее ядро колонок для OLTP-запросов и отдельный набор тяжелых атрибутов, которые нужны редко. Оно помогает ускорить основной read/write path, но добавляет стоимость join при восстановлении полной сущности.

## Что стоит раскрыть дальше

- [ ] Уточнить границу между vertical partitioning и нормализацией
- [ ] Добавить сценарии для wide tables и cold attributes
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
