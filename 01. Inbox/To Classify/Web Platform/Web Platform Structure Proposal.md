# Web Platform Structure Proposal

## Назначение

Этот файл фиксирует корневую смысловую иерархию для ветки `Web Platform` по правилам `Principia Rerum`.

Сейчас в `Inbox` уже есть несколько устойчивых web-platform кластеров:

- `Browser Page Processing`
- `Browser Loading Optimization Mechanisms`
- `Browser Rendering`
- `Web Origin Model`

Но у них пока нет общего корневого proposal-узла, который бы явно задавал дисциплинарную оптику и показывал рекомендуемую вложенность всей ветки.

## Выбранная оптика

Для этой ветки требуется зафиксировать и узаконить:

- `area: computer-science`
- `domain: web-platform`

`Web Platform` здесь понимается не как синоним всего frontend-разработческого мира, а как доменная рамка для browser-native механизмов, моделей безопасности, внутренних структур документа и процессов загрузки и отображения страницы.

Именно поэтому:

- `JavaScript` не стоит подчинять `Web Platform`, потому что это language-level ветка и для неё уже есть собственная рамка;
- `CSS` не стоит автоматически переносить под `Web Platform`, потому что в текущем корпусе это отдельная language-level styling branch;
- `HTTP` и его protocol-level семантика не стоит подчинять `Web Platform`, потому что это более естественная ветка внутри `networking`;
- `Frontend Engineering` остаётся более широкой прикладной рамкой, а `Web Platform` выступает как более узкий browser-platform domain внутри области computer science.

## Рекомендуемая иерархия

```text
Web Platform (overview)
├── Browser Page Processing (overview)
│   ├── Browser Loading Optimization Mechanisms (overview)
│   │   ├── Resource Hints (overview)
│   │   │   ├── DNS Prefetch (article)
│   │   │   ├── Preconnect (article)
│   │   │   ├── Preload (article)
│   │   │   ├── Prefetch (article)
│   │   │   └── Modulepreload (article)
│   │   ├── Early Hints (article)
│   │   ├── Fetch Priority (article)
│   │   ├── Lazy Loading (article)
│   │   ├── Script Loading and Execution Attributes (overview)
│   │   │   ├── HTML Script Async Attribute (article)
│   │   │   └── HTML Script Defer Attribute (article)
│   │   └── Speculation Rules API (article)
│   └── Browser Rendering (overview)
│       ├── DOM (article)
│       ├── CSSOM (article)
│       └── Browser Rendering Pipeline (overview)
│           ├── Render Tree (article)
│           ├── Layout (article)
│           ├── Paint (article)
│           └── Compositing (article)
└── Web Origin Model (overview)
    ├── Web Origin (article)
    ├── Same-Origin Policy (article)
    └── CORS (article)
```

## Почему структура именно такая

- `Web Platform` нужен как корневой `overview`, потому что в `Inbox` уже накопился не один isolated browser note, а несколько связанных подветок про единый класс browser-platform механизмов.
- `Browser Page Processing` оправдан как первый крупный `overview`, потому что он собирает процессы загрузки, подготовки и отображения страницы.
- `Browser Loading Optimization Mechanisms` и `Browser Rendering` лучше держать sibling-подветками внутри `Browser Page Processing`, потому что они описывают разные стадии и разные классы механизмов.
- `Web Origin Model` лучше держать отдельной sibling-веткой рядом с `Browser Page Processing`, а не прятать внутрь него, потому что это не стадия page processing, а самостоятельная security model браузерной платформы.
- `DOM` и `CSSOM` не стоит подчинять прямо `Web Platform`, потому что они естественно живут внутри `Browser Rendering`.
- `CORS` не стоит держать как отдельный корневой узел, потому что его смысл определяется только внутри `Web Origin Model`.

## Что не нужно создавать заранее

Пока не стоит заводить отдельные корневые заметки:

- `Web APIs`, если это будет просто слишком широкий контейнер без устойчивого корпуса;
- `Browser Internals`, если он будет дублировать уже выбранные `Browser Page Processing` и `Browser Rendering`;
- `Web Security` как корень для `CORS` и `Same-Origin Policy`, если пока речь идёт именно о browser origin model, а не о всей security surface веба;
- `HTML`, `CSS` и `JavaScript` как дочерние ветки `Web Platform`, потому что в текущей системе у них уже есть другие, более точные дисциплинарные рамки.

## Предлагаемое физическое размещение после нормализации

Если ветка будет доведена до канонического состояния и перенесена в `Corpus Mundi`, физическое размещение должно следовать алфавитному правилу:

```text
02. Corpus Mundi/
├── B/
│   ├── Browser Loading Optimization Mechanisms.md
│   ├── Browser Page Processing.md
│   ├── Browser Rendering.md
│   └── Browser Rendering Pipeline.md
├── C/
│   ├── CORS.md
│   ├── CSSOM.md
│   └── Compositing.md
├── D/
│   ├── DNS Prefetch.md
│   └── DOM.md
├── E/
│   └── Early Hints.md
├── F/
│   └── Fetch Priority.md
├── H/
│   ├── HTML Script Async Attribute.md
│   └── HTML Script Defer Attribute.md
├── L/
│   ├── Layout.md
│   └── Lazy Loading.md
├── M/
│   └── Modulepreload.md
├── P/
│   ├── Paint.md
│   ├── Prefetch.md
│   ├── Preconnect.md
│   └── Preload.md
├── R/
│   ├── Render Tree.md
│   └── Resource Hints.md
├── S/
│   ├── Same-Origin Policy.md
│   ├── Script Loading and Execution Attributes.md
│   └── Speculation Rules API.md
└── W/
    ├── Web Origin.md
    ├── Web Origin Model.md
    └── Web Platform.md
```

Логическая ветка при этом всё равно собирается через `parent`, `domain`, `section` и обычные `[[wikilinks]]`, а не через физическое соседство файлов.

## Что уже создано в Inbox

Уже существуют заметки для следующих подветок и статей:

- `Browser Loading Optimization Mechanisms`
- `Resource Hints`
- `Early Hints`
- `Fetch Priority`
- `Lazy Loading`
- `Script Loading and Execution Attributes`
- `Speculation Rules API`
- `Browser Rendering`
- `DOM`
- `CSSOM`
- `Browser Rendering Pipeline`
- `Render Tree`
- `Layout`
- `Paint`
- `Compositing`
- `Web Origin`
- `Same-Origin Policy`
- `CORS`

Пока отсутствуют как отдельные корневые overview-заметки:

- `Web Platform.md`
- `Browser Page Processing.md`
- `Web Origin Model.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Подтвердить `domain: web-platform` как устойчивое значение словаря, а не локальное исключение.
2. Создать корневой `overview` `Web Platform.md`.
3. Создать отсутствующие overview-заметки `Browser Page Processing.md` и `Web Origin Model.md`, чтобы текущие `parent`-связи перестали быть висячими.
4. Синхронизировать `Frontend Engineering` с новой корневой web-platform рамкой через `related`, а не через смешение доменов.
