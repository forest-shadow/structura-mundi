---
aliases:
  - TCP IP Model Structure Proposal
note_type: article
area: computer-science
domain: networking
section: network-models
parent: "[[Internet]]"
status: draft
related:
  - "[[Internet]]"
  - "[[TCP IP Model]]"
  - "[[OSI Model]]"
tags: []
---

# TCP IP Model Structure Proposal

## Краткое определение

Предлагаемое устройство ветки `TCP IP Model` внутри `Internet` как обзорной карты Internet protocol suite.

## Рекомендуемая иерархия

```text
Internet
└── TCP IP Model
    ├── TCP IP Link Layer
    ├── TCP IP Internet Layer
    ├── TCP IP Transport Layer
    └── TCP IP Application Layer
```

## Почему структура именно такая

- `TCP IP Model` служит обзорной рамкой для практической модели сетевого стека.
- Каждый слой является самостоятельным объектом знания и заслуживает собственной канонической статьи.
- Симметричное именование всех слоев внутри ветки делает ее более цельной и уменьшает вероятность путаницы.
- Более мелкие темы вроде `Encapsulation`, `Sockets`, `TCP vs UDP`, `TCP/IP vs OSI` пока лучше раскрывать как разделы внутри `TCP IP Model` или как будущие отдельные ветки, если накопится корпус.

## Что не нужно создавать заранее

- `TCP/IP vs OSI`, если это пока только сравнительный раздел
- `Layer 4`, `Layer 7` и прочие числовые дубли
- отдельные статьи на каждый протокол ради примеров слоя

## Что уже создано в ветке

- `[[TCP IP Model]]`
- `[[TCP IP Link Layer]]`
- `[[TCP IP Internet Layer]]`
- `[[TCP IP Transport Layer]]`
- `[[TCP IP Application Layer]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны `TCP`, `UDP` и `HTTP`
- [ ] Проверить `related`
