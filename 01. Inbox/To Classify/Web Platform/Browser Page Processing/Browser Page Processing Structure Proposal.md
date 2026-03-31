# Browser Page Processing Structure Proposal

## Назначение

Этот файл фиксирует общую смысловую иерархию для тем `Browser Loading Optimization Mechanisms` и `Browser Rendering` по правилам `Principia Rerum`.

Ветка пока размещена в `Inbox`, потому что для неё требуется расширение управляемого словаря:

- `area: computer-science`
- `domain: web-platform`
- `section: browser-page-processing`

`Browser Page Processing` здесь выступает не как ещё одна расплывчатая browser-тема, а как верхнеуровневая рамка для того, как браузер подготавливает, загружает и отображает страницу. Это позволяет держать `Browser Loading Optimization Mechanisms` и `Browser Rendering` в одной смысловой системе, не смешивая их в одну и ту же непосредственную подветку.

## Рекомендуемая иерархия

```text
Browser Page Processing (overview)
├── Browser Loading Optimization Mechanisms (overview)
│   ├── Resource Hints (overview)
│   ├── Fetch Priority (article)
│   └── Script Loading and Execution Attributes (overview)
└── Browser Rendering (overview)
    ├── DOM (article)
    ├── CSSOM (article)
    └── Browser Rendering Pipeline (overview)
```

## Почему структура именно такая

- `Browser Page Processing` достаточно широк, чтобы вместить и загрузку ресурсов, и последующее отображение страницы.
- При этом он не так двусмысленен, как `Browser Page Lifecycle`, который легко спутать с lifecycle вкладки, visibility state, bfcache и похожими темами.
- `Browser Loading Optimization Mechanisms` остаётся отдельной веткой про управление обнаружением ресурсов, приоритетами и стратегиями fetch/execute.
- Внутри этой ветки полезно явно отделять канонические `Resource Hints`, отдельный механизм `Fetch Priority` и атрибуты загрузки и исполнения `<script>`.
- `Browser Rendering` остаётся отдельной веткой про внутренние структуры и стадии визуального вывода.
- Связь между этими двумя ветками становится иерархически понятной, но их собственные границы не размываются.

## Что не нужно создавать заранее

Пока не стоит заводить отдельные заметки:

- `Browser Page Lifecycle`, если речь не идёт именно о lifecycle документа и вкладки;
- `Web Performance` как родительский узел для этой ветки, потому что это скорее поперечный аналитический срез, а не онтологический корень;
- `Critical Rendering Path` как обязательный соседний `overview`, если пока нет достаточного корпуса;
- промежуточные узлы вроде `Browser Internals` или `Page Display Pipeline`, если они дублируют уже выбранную рамку.

## Предлагаемое физическое размещение после нормализации

Если словарь будет расширен и заметки дойдут до канонического состояния, физическое размещение должно следовать алфавитному правилу:

```text
02. Corpus Mundi/
└── B/
    ├── Browser Page Processing.md
    ├── Browser Loading Optimization Mechanisms.md
    ├── Browser Rendering.md
    └── Browser Rendering Pipeline.md
```

Дочерние статьи из этих веток продолжают лежать в своих буквенных папках, а логическая иерархия собирается через `parent`.

## Созданные черновые заметки

- `Browser Page Processing.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Подтвердить `domain: web-platform`.
2. Подтвердить `section: browser-page-processing`.
3. Сохранить `Browser Loading Optimization Mechanisms` и `Browser Rendering` как отдельные подветки внутри общего узла.
4. Позже решить, когда внутри общего узла действительно назреют `HTML Parsing`, `CSS Processing` и `Critical Rendering Path`.


# Script Loading and Execution Attributes
## Что не входит в эту тему

- `Resource Hints`, потому что это отдельное семейство link-based hints.
- `Fetch Priority`, потому что это отдельный механизм влияния на приоритет загрузки.

## Что стоит раскрыть дальше

- [ ] Уточнить границу между classic scripts и module scripts
- [ ] Проверить, нужен ли позже отдельный узел про inline scripts