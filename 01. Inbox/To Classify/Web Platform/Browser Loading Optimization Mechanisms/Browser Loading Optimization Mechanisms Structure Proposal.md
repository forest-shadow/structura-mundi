# Browser Loading Optimization Mechanisms Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для темы `Browser Loading Optimization Mechanisms` внутри более общего узла `Browser Page Processing` по правилам `Principia Rerum`.

Ветка пока размещена в `Inbox`, потому что для неё требуется расширение управляемого словаря:

- `area: computer-science`
- `domain: web-platform`
- `section: browser-loading-optimization`
- `section: script-loading-and-execution`
- `section: resource-hints`
- `section: fetch-priority`

Здесь важно зафиксировать границу между каноническими именами и удобной рабочей рамкой. `Browser Loading Optimization Mechanisms` выступает как практическая надкатегория. Её иногда можно нестрого сокращать до `browser hints`, но внутри неё нужно различать более точные семейства и механизмы.

## Рекомендуемая иерархия

```text
Browser Page Processing (overview)
└── Browser Loading Optimization Mechanisms (overview)
    ├── Resource Hints (overview)
    │   ├── DNS Prefetch.md (article)
    │   ├── Preconnect.md (article)
    │   ├── Preload.md (article)
    │   ├── Prefetch.md (article)
    │   └── Modulepreload.md (article)
    ├── Early Hints.md (article)
    ├── Fetch Priority.md (article)
    ├── Lazy Loading.md (article)
    ├── Script Loading and Execution Attributes (overview)
    │   ├── HTML Script Async Attribute.md (article)
    │   └── HTML Script Defer Attribute.md (article)
    └── Speculation Rules API.md (article)
```

## Почему структура именно такая

- `Browser Loading Optimization Mechanisms` остаётся отдельной обзорной веткой и не маскирует различие между каноническими семействами и удобным зонтичным ярлыком.
- `Resource Hints` оправдан как вложенный `overview`, потому что это каноническое семейство link-based hints с собственной внутренней логикой.
- `Early Hints` не стоит прятать внутрь `Resource Hints`, потому что это HTTP-механизм ранней доставки подсказок через ответ `103`, а не отдельный link relation.
- `Fetch Priority` не стоит прятать внутрь `Resource Hints`, потому что это соседний механизм про приоритет, а не про раннее обнаружение ресурса.
- `Lazy Loading` лучше держать отдельной статьёй на уровне ветки, потому что это широкая стратегия отложенной загрузки для изображений, iframe и других некритичных ресурсов.
- `Script Loading and Execution Attributes` оправдан как вложенный `overview`, потому что `async` и `defer` образуют устойчивую маленькую группу с общими сравнениями и границами.
- `Speculation Rules API` не стоит прятать внутрь `Resource Hints`, потому что он описывает декларативный document-level prefetch и prerender для будущих навигаций.

## Что не нужно создавать заранее

Пока не стоит заводить отдельные заметки:

- `Browser Hints` как будто бы канонический родительский узел, потому что это слишком расплывчатое и нестрогое имя;
- `Async vs Defer`, если сравнение можно удержать внутри `Script Loading and Execution Attributes`;
- широкую ветку `Web Performance`, если она нужна только как контейнер для этой темы;
- отдельные статьи на все возможные loading-related signals без устойчивой понятийной границы.

## Предлагаемое физическое размещение после нормализации

Если словарь будет расширен и заметки дойдут до канонического состояния, физическое размещение должно следовать алфавитному правилу:

```text
02. Corpus Mundi/
├── A/
│   └── Async Script.md
├── B/
│   └── Browser Loading Optimization Mechanisms.md
├── D/
│   ├── Defer Script.md
│   └── DNS Prefetch.md
├── E/
│   └── Early Hints.md
├── F/
│   └── Fetch Priority.md
├── L/
│   └── Lazy Loading.md
├── M/
│   └── Modulepreload.md
├── P/
│   ├── Prefetch.md
│   ├── Preconnect.md
│   └── Preload.md
├── R/
│   └── Resource Hints.md
└── S/
    ├── Script Loading and Execution Attributes.md
    └── Speculation Rules API.md
```

Логическая ветка при этом всё равно собирается через `parent`.

## Созданные черновые заметки

- `Browser Loading Optimization Mechanisms.md`
- `Resource Hints.md`
- `DNS Prefetch.md`
- `Preconnect.md`
- `Preload.md`
- `Prefetch.md`
- `Modulepreload.md`
- `Early Hints.md`
- `Fetch Priority.md`
- `Lazy Loading.md`
- `Script Loading and Execution Attributes.md`
- `Async Script.md`
- `Defer Script.md`
- `Speculation Rules API.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Подтвердить `domain: web-platform`.
2. Подтвердить `section: browser-loading-optimization`.
3. Подтвердить `section: resource-hints`, `section: fetch-priority` и `section: script-loading-and-execution`.
4. Синхронизировать ветку с общим узлом `Browser Page Processing`.
5. Уточнить понятийные границы между `Preload` и `Early Hints`, а также между `Prefetch` и `Speculation Rules API`.
