---
aliases:
  - Packet Switches Structure Proposal
note_type: article
area: computer-science
domain: networking
section: packet-switches
parent: "[[Networking]]"
status: draft
related:
  - "[[Networking]]"
  - "[[Packet Switches]]"
  - "[[Router]]"
  - "[[Link-Layer Switch]]"
tags: []
---

# Packet Switches Structure Proposal

## Краткое определение

Предлагаемое устройство ветки `Packet Switches` внутри domain `networking`.

## Рекомендуемая иерархия

```text
Networking
└── Packet Switches
    ├── Router
    └── Link-Layer Switch
```

## Почему структура именно такая

- `Packet Switches` оправдан как `sub-overview`, потому что router и link-layer switch образуют маленький, но устойчивый кластер forwarding devices.
- `Router` и `Link-Layer Switch` лучше держать sibling-статьями, потому что их полезно сравнивать рядом: inter-network forwarding против frame switching внутри локального сегмента.
- Тему не стоит раскладывать только по слоям `OSI`, потому что тогда теряется общая device-level рамка.

## Что не стоит делать прямо сейчас

- не смешивать сюда `Routing Protocols`, потому что это control-plane protocols, а не forwarding devices;
- не создавать сразу плоский каталог всех сетевых устройств;
- не заводить отдельные template-файлы под packet-switching-ветку.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны `Switching Fabric`, `Forwarding Table` и `Bridge`
- [ ] Проверить, не нужен ли позже отдельный узел про `Packet Forwarding`
- [ ] Проверить `related`
