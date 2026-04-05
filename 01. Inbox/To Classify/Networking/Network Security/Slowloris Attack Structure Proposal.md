---
aliases:
  - Slowloris Branch Structure Proposal
  - Структура ветки Slowloris Attack
note_type: article
area: computer-science
domain: networking
section: network-security
parent: "[[Network Security]]"
status: draft
related:
  - "[[Network Security]]"
  - "[[Slowloris Attack]]"
  - "[[HTTP]]"
  - "[[Timeouts and Cancellation]]"
  - "[[Server Resource Management]]"
  - "[[Go Servers]]"
tags: []
---

# Slowloris Attack Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для темы `Slowloris Attack` внутри `Network Security` по правилам `Principia Rerum`.

Для этой темы не требуется новый `section`:

- `area: computer-science`
- `domain: networking`
- `section: network-security` (переиспользуем существующее значение)

## Рекомендуемая иерархия

```text
Networking
└── Network Security
    └── Slowloris Attack
```

Переиспользуемые соседние заметки:

- `HTTP`
- `Timeouts and Cancellation`
- `Server Resource Management`

## Почему структура именно такая

- `Slowloris Attack` лучше оформлять как отдельную `article`, а не как дочернюю тему `HTTP`, потому что здесь важна не спецификация протокола сама по себе, а security-оптика на атаку истощения ресурсов.
- Тему не стоит подчинять `Server Process` или `Timeouts and Cancellation`, потому что эти заметки описывают защитные и operational механизмы, а не сам класс атаки.
- Отдельный `overview` вроде `Denial-of-Service Attacks` пока преждевременен: для него еще нет плотного корпуса соседних заметок вроде `SYN Flood`, `HTTP Flood` или `Amplification Attack`.
- Ветка естественно живет внутри `Network Security`, потому что описывает вектор атаки на сетевое и прикладное взаимодействие между клиентом и сервером.

## Что не нужно создавать заранее

Пока не стоит заводить отдельные узлы:

- `Denial-of-Service Attacks` как обязательный промежуточный `overview`;
- `Slow HTTP Attacks` как дополнительный уровень ради одной статьи;
- vendor-specific заметки вроде `Nginx Slowloris Mitigation` или `Apache Slowloris Protection`;
- отдельные template-файлы под security-attack notes, потому что по `Principia Rerum` здесь достаточно канонических `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение после нормализации

Если заметка дойдет до канонического состояния, её физическое размещение должно следовать алфавитному правилу:

```text
02. Corpus Mundi/
└── S/
    └── Slowloris Attack.md
```

Локальные вложения при необходимости:

```text
02. Corpus Mundi/S/_resources/Slowloris Attack/
```

## Созданные черновые заметки

- `Slowloris Attack.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Проверить границу между `Slowloris Attack` как security-темой и `Timeouts and Cancellation` как защитным operational механизмом.
2. Решить, когда в `Network Security` оправдан отдельный обзорный узел для DoS- и DDoS-атак.
3. После этого перевести заметку из `seed` в рабочий черновик и наполнить содержанием.
