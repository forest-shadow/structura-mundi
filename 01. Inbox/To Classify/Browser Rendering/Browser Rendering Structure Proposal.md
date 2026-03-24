# Browser Rendering Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для темы `Browser Rendering` и вложенного понятия `Browser Rendering Pipeline` внутри более общего узла `Browser Page Processing` по правилам `Principia Rerum`.

Ветка пока размещена в `Inbox`, потому что для неё требуется расширение управляемого словаря:

- `area: computer-science`
- `domain: web-platform` (уже предлагается в соседних web-platform ветках)
- `section: browser-rendering` (предлагаемое новое значение)
- `section: browser-rendering-pipeline` (предлагаемое новое значение для устойчивой дочерней подветки)

`Browser Rendering Pipeline` не стоит держать как одну изолированную статью без более широкой рамки, потому что рядом с ним находятся разные по типу сущности: базовые структуры (`DOM`, `CSSOM`), производная структура (`Render Tree`) и собственно стадии вывода (`Layout`, `Paint`, `Compositing`). Для такой темы достаточно одного корневого `overview` и одного оправданного вложенного `overview`.

## Рекомендуемая иерархия

```text
Browser Page Processing (overview)
└── Browser Rendering (overview)
    ├── DOM (article)
    ├── CSSOM (article)
    └── Browser Rendering Pipeline (overview)
        ├── Render Tree (article)
        ├── Layout (article)
        ├── Paint (article)
        └── Compositing (article)
```

## Почему структура именно такая

- `Browser Rendering` остаётся отдельной обзорной веткой, но теперь естественно подчиняется более общему узлу `Browser Page Processing`.
- `DOM` и `CSSOM` лучше держать прямыми дочерними статьями `Browser Rendering`, а не подчинять их `Browser Rendering Pipeline`, потому что это более широкие платформенные структуры, а не только стадии конвейера.
- `Browser Rendering Pipeline` оправдан как вложенный `overview`, потому что внутри него есть устойчивый набор дочерних тем: `Render Tree`, `Layout`, `Paint`, `Compositing`.
- `Render Tree` полезно держать отдельной статьёй, потому что это мост между входными структурами (`DOM`, `CSSOM`) и последующими стадиями вывода.
- `Layout`, `Paint` и `Compositing` заслуживают отдельных канонических статей, потому что это самостоятельные стадии с разными причинами стоимости, инвалидации и оптимизации.
- Дополнительная глубина пока не нужна: темы вроде `Reflow`, `Repaint`, `Layer Tree`, `Rasterization` и `Critical Rendering Path` можно сначала раскрывать как разделы внутри существующих заметок или добавлять позже, если ветка реально вырастет.

## Что не нужно создавать заранее

Пока не стоит заводить отдельные заметки:

- `HTML Parsing` и `CSS Parsing`, если они пока нужны только как вводные шаги внутри обзорной заметки;
- `Reflow` и `Repaint` как отдельные канонические узлы, если их можно сначала раскрыть внутри `Layout` и `Paint`;
- отдельный `Rendering Performance` overview, если он нужен только ради этой ветки;
- дополнительный промежуточный `overview` между `Browser Rendering` и `Browser Rendering Pipeline`.

## Предлагаемое физическое размещение после нормализации

Если словарь будет расширен и заметки дойдут до канонического состояния, физическое размещение должно следовать алфавитному правилу:

```text
02. Corpus Mundi/
├── B/
│   ├── Browser Rendering.md
│   └── Browser Rendering Pipeline.md
├── C/
│   ├── CSSOM.md
│   └── Compositing.md
├── D/
│   └── DOM.md
├── L/
│   └── Layout.md
├── P/
│   └── Paint.md
└── R/
    └── Render Tree.md
```

Логическая ветка при этом всё равно собирается через `parent`.

## Созданные черновые заметки

- `Browser Rendering.md`
- `DOM.md`
- `CSSOM.md`
- `Browser Rendering Pipeline.md`
- `Render Tree.md`
- `Layout.md`
- `Paint.md`
- `Compositing.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Подтвердить `domain: web-platform`.
2. Подтвердить `section: browser-rendering`.
3. Решить, сохранять ли отдельный `section: browser-rendering-pipeline` или оставить всю ветку в одном общем `section`, если она останется компактной.
4. Синхронизировать ветку с общим узлом `Browser Page Processing`.
5. Наполнить `Browser Rendering` так, чтобы различие между входными структурами и стадиями пайплайна было видно уже из overview.
