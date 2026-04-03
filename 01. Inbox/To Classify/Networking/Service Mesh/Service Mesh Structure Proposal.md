---
aliases:
  - Service Mesh Structure Proposal
  - Структура ветки Service Mesh
note_type: article
area: computer-science
domain: networking
section: traffic-intermediation
parent: "[[Networking]]"
status: draft
related:
  - "[[Networking]]"
  - "[[Service Mesh]]"
  - "[[Istio]]"
  - "[[Proxy]]"
  - "[[Layer 7 Proxy]]"
  - "[[TLS Termination]]"
tags: []
---

# Service Mesh Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для темы `Service Mesh`, в которую естественно помещается рассмотрение такого понятия, как `Istio`, по правилам `Principia Rerum`.

## Выбранная оптика

- `area: computer-science`
- `domain: networking`
- `section: traffic-intermediation` (уже используемое рабочее значение)

Почему так:

- `Service Mesh` естественно продолжает уже существующий сетевой кластер `traffic-intermediation`, где рядом живут `Proxy`, `TLS Termination` и `Origin Shielding`;
- `Istio` здесь важен прежде всего как конкретная реализация service-mesh-подхода, а не как отдельный домен знания;
- новый `section` вводить не нужно, потому что существующий рабочий кластер уже покрывает эту тему достаточно точно.

## Канонические имена

- section-level overview: `Service Mesh`
- articles:
  - `Service Mesh Control Plane`
  - `Service Mesh Data Plane`
  - `Istio`

## Рекомендуемая иерархия

```text
Networking
└── Service Mesh
    ├── Service Mesh Control Plane
    ├── Service Mesh Data Plane
    └── Istio
```

## Почему структура именно такая

- `Service Mesh` лучше сделать `overview`, потому что это не один механизм, а устойчивый инфраструктурный кластер тем: control plane, data plane, traffic policy, mTLS, observability и service-to-service routing.
- `Service Mesh` не стоит подчинять `Proxy`, потому что proxy является лишь одним из строительных блоков mesh, тогда как сама тема включает еще централизованное управление политиками и конфигурацией.
- `Service Mesh Control Plane` и `Service Mesh Data Plane` полезно оформить как отдельные обычные `article`, потому что именно через это различение обычно объясняется устройство mesh-систем.
- `Istio` на текущем этапе лучше держать как обычную `article`, а не как отдельный product-specific overview, потому что пока еще нет устойчивого корпуса дочерних заметок вроде `Istio VirtualService`, `Istio DestinationRule` или `Istio Gateway`.

## Что не стоит делать прямо сейчас

- Не стоит помещать `Istio` напрямую под `Networking`, потому что так теряется service-mesh-контекст.
- Не стоит помещать `Istio` внутрь `Proxy`, потому что это создает ложную редукцию mesh к одному лишь proxy-layer.
- Не стоит заранее заводить sibling-vendor notes вроде `Linkerd` или `Consul Connect`, пока нет реального корпуса по service mesh как семейству решений.
- Не стоит создавать отдельные тематические template-файлы под эту ветку: по `Principia Rerum` здесь достаточно канонических `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
├── I/
│   └── Istio.md
└── S/
    ├── Service Mesh.md
    ├── Service Mesh Control Plane.md
    └── Service Mesh Data Plane.md
```

## Что уже создано в Inbox

- `[[Service Mesh]]`
- `[[Service Mesh Control Plane]]`
- `[[Service Mesh Data Plane]]`
- `[[Istio]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом с `Istio` нужны product-specific notes про traffic management и security policy
- [ ] Проверить границу между `Service Mesh`, `Proxy`, `API Gateway` и `Load Balancer`
- [ ] Проверить `related`
