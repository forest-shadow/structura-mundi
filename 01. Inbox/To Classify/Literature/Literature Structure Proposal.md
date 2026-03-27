---
aliases:
  - Literature Structure Proposal
note_type: article
area: literature
domain: literary-studies
section:
parent:
status: draft
related:
  - "[[Literature]]"
  - "[[Russian Literature]]"
  - "[[Viktor Pelevin]]"
tags: []
---

# Literature Structure Proposal

## Краткое определение

Предлагаемое устройство ветки `Literature` внутри общей гуманитарной части vault.

## Рекомендуемая иерархия

```text
Literature
└── Russian Literature
    └── Viktor Pelevin
        ├── Viktor Pelevin Biography and Literary Context
        ├── Viktor Pelevin Themes and Motifs
        ├── Viktor Pelevin Style and Poetics
        └── Viktor Pelevin Works
```

## Почему структура именно такая

- `Literature` оправдана как новый root-domain, потому что тема не сводится к одному автору и требует хотя бы национальных и авторских подветок.
- `Russian Literature` лучше создавать как промежуточный `sub-overview`, чтобы не смешивать авторов разных литературных традиций в одном плоском списке.
- `Viktor Pelevin` уже оправдан как отдельная author-ветка, потому что обсуждение автора естественно распадается на биографический контекст, поэтику, мотивы и корпус произведений.
- Отдельные notes про конкретные романы пока не создаются, чтобы сначала собрать минимальную устойчивую авторскую карту.

## Что не стоит делать прямо сейчас

- Не стоит класть `Viktor Pelevin` прямо под `Literature` без уровня `Russian Literature`.
- Не стоит заранее плодить отдельные notes про каждое произведение без авторского overview и работоспособной авторской ветки.
- Не стоит смешивать биографию автора, анализ поэтики и список произведений в одной неструктурированной статье.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны другие авторские ветки внутри `Russian Literature`
- [ ] Проверить, нужен ли отдельный узел про `Contemporary Russian Literature`
- [ ] Проверить `related`
