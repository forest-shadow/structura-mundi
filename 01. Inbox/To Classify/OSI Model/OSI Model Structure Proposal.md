---
aliases:
  - OSI Model Structure Proposal
note_type: article
area: computer-science
domain: networking
section: network-models
parent: "[[Networking]]"
status: draft
related:
  - "[[Networking]]"
  - "[[OSI Model]]"
  - "[[Internet]]"
tags: []
---

# OSI Model Structure Proposal

## Краткое определение

Предлагаемое устройство ветки `OSI Model` внутри domain `networking` как отдельной концептуальной model-ветки.

## Рекомендуемая иерархия

```text
Networking
└── OSI Model
    ├── Physical Layer
    ├── Data Link Layer
    ├── Network Layer
    ├── Transport Layer
    ├── Session Layer
    ├── Presentation Layer
    └── Application Layer
```

## Почему структура именно такая

- `OSI Model` служит обзорной картой для всей модели и позволяет объяснить назначение каждого слоя в общей архитектуре.
- Каждый слой является самостоятельным объектом знания и заслуживает собственной канонической статьи.
- Дополнительные подветки вроде `Encapsulation`, `Protocol Data Units` или `Layer Interaction` пока не нужны: их можно раскрывать как разделы внутри `OSI Model` или внутри статей по слоям.
- Ветка остается плоской и предсказуемой, что соответствует правилу минимальной вложенности.

## Что не нужно создавать заранее

- `OSI vs TCP/IP`, если это пока только сравнительный раздел внутри `OSI Model`
- `Encapsulation in OSI Model`, если это пока не тянет на самостоятельную статью
- `Layer 2`, `Layer 3`, `Layer 4` как дубли канонических имен слоев

## Что уже создано в ветке

- `[[OSI Model]]`
- `[[Physical Layer]]`
- `[[Data Link Layer]]`
- `[[Network Layer]]`
- `[[Transport Layer]]`
- `[[Session Layer]]`
- `[[Presentation Layer]]`
- `[[Application Layer]]`

## Что стоит раскрыть дальше

- [ ] Уточнить границы между `OSI Model` и `Internet`
- [ ] Проверить `related`
