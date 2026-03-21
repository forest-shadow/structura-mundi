# Browser Loading Hints Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для темы `Browser Loading Hints` по правилам `Principia Rerum`.

Ветка пока размещена в `Inbox`, потому что для неё требуется расширение управляемого словаря:

- `area: computer-science`
- `domain: web-platform` (уже предлагается в соседних web-platform ветках)
- `section: browser-loading-hints` (предлагаемое новое значение)
- `section: script-loading` (предлагаемое новое значение для устойчивой дочерней подветки)
- `section: resource-hints` (предлагаемое новое значение для устойчивой дочерней подветки)

Тема не должна быть одной общей статьёй про всё сразу. `async` и `defer` относятся к поведению `<script>`, а `preload`, `prefetch`, `modulepreload` относятся к сетевым и загрузочным подсказкам браузеру. Для энциклопедической ветки полезно держать их внутри одной общей рамки, но с явным разделением на два устойчивых кластера.

## Рекомендуемая иерархия

```text
Browser Loading Hints (overview)
├── Script Loading Attributes (overview)
│   ├── Async Script.md (article)
│   └── Defer Script.md (article)
└── Resource Hints (overview)
    ├── Preload.md (article)
    ├── Prefetch.md (article)
    └── Modulepreload.md (article)
```

## Почему структура именно такая

- `Browser Loading Hints` даёт общую рамку для механизмов, которыми разработчик подсказывает браузеру порядок, приоритет или стратегию загрузки.
- `Script Loading Attributes` оправдан как вложенный `overview`, потому что `async` и `defer` образуют устойчивую маленькую группу с общими границами и сравнениями.
- `Resource Hints` тоже оправдан как вложенный `overview`, потому что `preload`, `prefetch` и `modulepreload` относятся к другому классу механизмов и не должны смешиваться с поведением `<script>`.
- Более глубокая вложенность пока не нужна: отдельные темы вроде `fetchpriority` или `preconnect` можно добавить позже, если ветка действительно вырастет.

## Что не нужно создавать заранее

Пока не стоит заводить отдельные заметки:

- `Script Tag Loading` как дополнительный промежуточный слой между `Browser Loading Hints` и `Script Loading Attributes`;
- отдельную заметку `Async vs Defer`, если это можно раскрыть внутри `Script Loading Attributes`;
- отдельные статьи на все возможные performance hints браузера;
- отдельную широкую ветку `Web Performance`, если она нужна только ради этой темы.

## Предлагаемое физическое размещение после нормализации

Если словарь будет расширен и заметки дойдут до канонического состояния, физическое размещение должно следовать алфавитному правилу:

```text
02. Corpus Mundi/
├── A/
│   └── Async Script.md
├── B/
│   └── Browser Loading Hints.md
├── D/
│   └── Defer Script.md
├── M/
│   └── Modulepreload.md
├── P/
│   ├── Prefetch.md
│   └── Preload.md
├── R/
│   └── Resource Hints.md
└── S/
    └── Script Loading Attributes.md
```

Логическая ветка при этом всё равно собирается через `parent`.

## Созданные черновые заметки

- `Browser Loading Hints.md`
- `Script Loading Attributes.md`
- `Async Script.md`
- `Defer Script.md`
- `Resource Hints.md`
- `Preload.md`
- `Prefetch.md`
- `Modulepreload.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Подтвердить `domain: web-platform`.
2. Подтвердить `section: browser-loading-hints`.
3. Подтвердить `section: script-loading` и `section: resource-hints`, если они окажутся полезными не только для одной ветки.
4. Наполнить `Browser Loading Hints` так, чтобы граница между script-loading и resource-hints была явно различима.
