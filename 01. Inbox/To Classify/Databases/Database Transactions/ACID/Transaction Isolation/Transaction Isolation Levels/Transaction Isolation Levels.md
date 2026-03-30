---
aliases:
  - Уровни изоляции транзакций
note_type: overview
area: computer-science
domain: databases
section: transactions
parent: "[[Transaction Isolation]]"
status: seed
related:
  - "[[ACID]]"
  - "[[Database Transactions]]"
  - "[[Transaction Isolation]]"
  - "[[Isolation Anomalies]]"
  - "[[Snapshot Isolation]]"
tags:
  - transactions
  - consistency
---

# Transaction Isolation Levels

## Краткое определение области

Обзорная заметка для уровней изоляции транзакций, их компромиссов и тех аномалий конкурентного доступа, которые они допускают или предотвращают.

## Что входит в эту тему

- `[[Isolation Anomalies]]`
- `[[Read Uncommitted]]`
- `[[Read Committed]]`
- `[[Repeatable Read]]`
- `[[Serializable]]`
- `[[Snapshot Isolation]]`

## Как устроена ветка

- `Isolation Anomalies` задает проблемную рамку.
- Конкретные уровни изоляции раскрываются как отдельные `article`.
- Дополнительный `sub-overview` пока не нужен.

## Рекомендуемый маршрут чтения

1. Начать с `[[Isolation Anomalies]]`.
2. Затем пройти классические уровни изоляции от `[[Read Uncommitted]]` к `[[Serializable]]`.
3. После этого посмотреть `[[Snapshot Isolation]]` как важный практический вариант вне простой линейной шкалы.

## Соседние overview-ветки

- Пока не добавлены.

## Что стоит раскрыть дальше

- [ ] Проверить границы темы
- [ ] Проверить дочерние статьи
- [ ] Проверить `related`
- [ ] Не разрастается ли ветка слишком глубоко
