
## Краткое определение

Предлагаемое устройство ветки `Internet` внутри domain `networking`.

## Рекомендуемая иерархия

```text
Networking
└── Internet
    ├── Network Edge
    │   ├── End System
    │   └── Access Network
    ├── TCP IP Model
    │   ├── TCP IP Link Layer
    │   ├── TCP IP Internet Layer
    │   ├── TCP IP Transport Layer
    │   └── TCP IP Application Layer
    ├── IP Addressing
    ├── Routing
    └── DNS
        ├── DNS Resolution
        ├── Recursive Resolver
        ├── Authoritative DNS Server
        ├── DNS Resource Record
        └── DNS Zone
```

## Почему структура именно такая

- `Internet` уже оправдан как `sub-overview`, потому что рассмотрение Internet не сводится к одному определению и требует хотя бы адресации, маршрутизации, naming и протокольной архитектуры.
- `Network Edge` логично делать дочерней overview-веткой именно внутри `Internet`, потому что понятие edge здесь устойчиво связывает hosts и access networks в одну локальную рамку.
- `End System` лучше оформлять как обычную article-note, потому что это одно устойчивое понятие, а desktops, smartphones и servers пока достаточно держать как примеры внутри него, а не как отдельные дочерние заметки.
- `Access Network` логично держать рядом с `End System`, потому что она описывает не конечную систему, а способ ее включения в Internet.
- `TCP IP Model` логично делать дочерней overview-веткой именно `Internet`, потому что Internet protocol suite описывает архитектурный стек самой Internet.
- `IP Addressing` и `Routing` достаточно самостоятельны для отдельных article-notes и пока не требуют промежуточных overview-узлов.
- `DNS` уже лучше оформлять как отдельный `sub-overview`, потому что внутри него быстро возникает собственный устойчивый кластер: resolution, resolver role, authoritative role и базовые сущности данных.

## Что не стоит делать прямо сейчас

- Не стоит заводить отдельные заметки под `Desktop`, `Smartphone` и `Server` внутри Internet-ветки, пока `End System` покрывает их как один устойчивый класс hosts.
- Не стоит переносить сюда `Server Host`, потому что в существующей системе знаний он уже живет в role-centric ветке `Client-Server Model`.
- Не стоит заранее выносить `TCP`, `UDP`, `HTTP`, `BGP` и `NAT` в отдельные article без плотного корпуса рядом.
- Не стоит смешивать Internet branch с purely conceptual `OSI Model`.
- Не стоит преждевременно дробить DNS еще глубже на `Root Name Server`, `DNSSEC` и `Zone Transfer`, пока базовая DNS-ветка не наполнена.

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом с `Network Edge` нужен `Network Core`
- [ ] Решить, когда внутри `Access Network` нужны более конкретные виды сетей доступа
- [ ] Решить, когда нужны `TCP`, `UDP` и `HTTP`
- [ ] Подтвердить, нужен ли для DNS отдельный `section: dns`
- [ ] Проверить `related`
