---
aliases:
  - DNS Structure Proposal
note_type: article
area: computer-science
domain: networking
section: dns
parent: "[[Internet]]"
status: draft
related:
  - "[[DNS]]"
  - "[[Internet]]"
  - "[[DNS Resolution]]"
  - "[[Recursive Resolver]]"
  - "[[Authoritative DNS Server]]"
tags: []
---

# DNS Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для темы `DNS` по правилам `Principia Rerum`.

Ветка пока размещена в `Inbox`, потому что для нее предлагается новое значение `section`:

- `area: computer-science`
- `domain: networking`
- `section: dns` (предлагаемое новое значение)

`domain` уже используется в networking-ветке. Новым здесь является только `section`, и его имеет смысл вводить не ради одной заметки, а ради устойчивого кластера тем о разрешении имен, ролях DNS-узлов и модели данных DNS.

## Рекомендуемая иерархия

```text
Internet
└── DNS
    ├── DNS Resolution
    ├── Recursive Resolver
    ├── Authoritative DNS Server
    ├── DNS Resource Record
    └── DNS Zone
```

## Почему структура именно такая

- `DNS` уже оправдан как `sub-overview`, потому что тема не сводится к одной обзорной статье и внутри нее есть как минимум процесс разрешения имен, роли серверов и отдельный слой данных.
- `DNS Resolution` лучше держать отдельной статьей, потому что это центральный механизм ветки, вокруг которого потом естественно группируются рекурсия, кэширование и делегирование.
- `Recursive Resolver` и `Authoritative DNS Server` нужно разделять, потому что это разные роли в системе с разными задачами и границами ответственности.
- `DNS Resource Record` и `DNS Zone` образуют минимальный понятийный слой, без которого DNS-ветка остается только описанием сетевого процесса без структуры данных.
- Глубже ветку сейчас дробить не нужно: отдельные узлы про `Root Name Server`, `TLD Name Server`, `DNSSEC` или `Zone Transfer` пока будут преждевременны.

## Что пока не нужно создавать

- `Root Name Server` как отдельную заметку, если пока достаточно описания внутри `DNS Resolution`
- `TLD Name Server` как отдельную заметку, если тема еще не вышла за рамки общей схемы делегирования
- `DNSSEC` как отдельную ветку, если еще не формируется устойчивый security-подкластер
- `Zone Transfer` и `TTL` как отдельные статьи, если они пока нужны только как локальные разделы

## Созданные черновые заметки

- `DNS.md`
- `DNS Resolution.md`
- `Recursive Resolver.md`
- `Authoritative DNS Server.md`
- `DNS Resource Record.md`
- `DNS Zone.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Подтвердить `section: dns` как рабочий тематический кластер внутри `domain: networking`.
2. Решить, нужны ли рядом отдельные статьи про `TTL`, `DNS Caching` и `DNSSEC`, или пока достаточно локальных разделов внутри базовых заметок.
3. После этого перевести seed-заметки в содержательные черновики и нормализовать `related`.
