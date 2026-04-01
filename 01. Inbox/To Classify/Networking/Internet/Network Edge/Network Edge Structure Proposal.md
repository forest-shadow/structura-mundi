# Network Edge Structure Proposal

## Краткое определение

Предлагаемое место для `Network Edge` внутри ветки `Internet` как отдельного `sub-overview`, в который естественно помещаются `End System` и `Access Network`.

## Рекомендуемая иерархия

```text
Networking
└── Internet
    └── Network Edge
        ├── End System
        └── Access Network
```

## Почему структура именно такая

- `Network Edge` оправдан как `sub-overview`, потому что тема не сводится к одной статье про hosts: здесь устойчиво соседствуют оконечные системы и способы их подключения к Internet.
- `End System` лучше оформлять как отдельную `article`, потому что это устойчивое сетевое понятие про hosts на границе сети, а не просто список устройств.
- `Access Network` логично держать sibling-заметкой рядом с `End System`, потому что она описывает не сам host, а last-hop среду, через которую host получает доступ к Internet.
- `Server` не стоит делать дочерней заметкой внутри этой ветки, потому что в vault он уже живет в role-centric рамке `Client-Server Model`, а в контексте `Network Edge` сервер выступает только как один из видов host.

## Что не стоит делать прямо сейчас

- Не стоит заводить отдельные заметки под `Desktop`, `Smartphone` или `IoT Device`, пока это лишь примеры внутри более общего понятия `End System`.
- Не стоит переносить сюда `Server Host`, потому что это создаст дублирование между role-centric и Internet-centric иерархиями.
- Не стоит создавать специальный template-файл под `Network Edge`, потому что по `Principia Rerum` достаточно канонических `Overview Template` и `Article Template`.

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом с `Network Edge` нужен `Network Core`
- [ ] Решить, когда внутри `Access Network` нужны `Home Network`, `Enterprise Access Network` и `Mobile Access Network`
- [ ] Проверить будущие `related`
