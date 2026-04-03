---
aliases: []
note_type: article
area: computer-science
domain: distributed-systems
section: kafka
parent: "[[Kafka]]"
status: seed
related:
  - "[[Kafka Topic]]"
  - "[[Kafka Partition]]"
  - "[[Kafka Consumer Group]]"
  - "[[Idempotent Consumer]]"
tags: []
---

# Kafka Offset

## Краткое определение

`Kafka Offset` — это позиция записи внутри конкретного partition, через которую Kafka адресует сообщения и отслеживает прогресс чтения потребителей.

## Основная идея или механизм

Нужно раскрыть, как offset связывает модель хранения с моделью чтения, почему commit offsets влияет на delivery semantics и как это связано с повторной обработкой сообщений.

## Границы темы

- Что относится к offset как позиции в partition log.
- Чем offset отличается от message id, sequence number и внешней бизнес-идентичности события.

## Связи с другими заметками

Родительская тема:

`[[Kafka]]`

Связанные заметки:

- `[[Kafka Topic]]`
- `[[Kafka Partition]]`
- `[[Kafka Consumer Group]]`
- `[[Idempotent Consumer]]`

## Примеры, случаи или следствия

Добавить 1-3 примера offset commit, replay и влияния на at-least-once behavior.

## Что стоит раскрыть дальше

- [ ] Уточнить определение
- [ ] Добавить связи
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
