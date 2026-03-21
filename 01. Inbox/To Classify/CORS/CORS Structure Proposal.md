# CORS Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для темы `CORS` по правилам `Principia Rerum`.

Ветка пока размещена в `Inbox`, потому что для неё требуется расширение управляемого словаря:

- `area: computer-science`
- `domain: web-platform` (предлагаемое новое значение)
- `section: web-origin-model` (предлагаемое новое значение)
- `section: cors` (предлагаемое новое значение для устойчивой дочерней подветки)

`CORS` не стоит держать как одиночную статью без окружающей рамки, потому что его смысл определяется через `origin`, `same-origin policy` и механизм предварительной проверки запросов. При этом не нужно создавать слишком глубокое дерево: достаточно одного корневого `overview` и одной оправданной вложенной `overview`-ветки.

## Рекомендуемая иерархия

```text
Web Origin Model (overview)
├── Web Origin (article)
├── Same-Origin Policy (article)
└── CORS (overview)
    ├── Preflight Request (article)
    ├── CORS Request Headers (article)
    ├── CORS Response Headers (article)
    └── Credentialed CORS Requests (article)
```

## Почему структура именно такая

- `Web Origin Model` даёт правильную верхнеуровневую рамку для origin-based ограничений браузера.
- `Web Origin` нужен как отдельная статья, потому что без него тема `CORS` быстро превращается в набор частных правил без базового объекта.
- `Same-Origin Policy` следует держать рядом как самостоятельную каноническую статью, а не растворять внутри `CORS`.
- `CORS` оправдан как вложенный `overview`, потому что вокруг него есть устойчивый набор дочерних механизмов: preflight, request headers, response headers, credentialed requests.
- Более глубокая вложенность пока не нужна: отдельные узлы вроде `Access-Control-Allow-Origin` или `Origin`-header можно сначала раскрывать внутри существующих статей.

## Что не нужно создавать заранее

Пока не стоит заводить отдельные заметки:

- `Simple Request`, если это будет только исторический ярлык внутри статьи про `CORS`;
- отдельные статьи на каждый CORS-заголовок;
- дополнительный промежуточный `overview` между `Web Origin Model` и `CORS`;
- отдельную ветку `Browser Security`, если она пока нужна только ради одной темы.

Эти узлы можно добавить позже, если ветка действительно вырастет.

## Предлагаемое физическое размещение после нормализации

Если словарь будет расширен и заметки дойдут до канонического состояния, физическое размещение должно следовать алфавитному правилу:

```text
02. Corpus Mundi/
├── C/
│   ├── CORS.md
│   ├── CORS Request Headers.md
│   ├── CORS Response Headers.md
│   └── Credentialed CORS Requests.md
├── P/
│   └── Preflight Request.md
├── S/
│   └── Same-Origin Policy.md
└── W/
    ├── Web Origin.md
    └── Web Origin Model.md
```

Логическая ветка при этом всё равно собирается через `parent`.

## Созданные черновые заметки

- `Web Origin Model.md`
- `Web Origin.md`
- `Same-Origin Policy.md`
- `CORS.md`
- `Preflight Request.md`
- `CORS Request Headers.md`
- `CORS Response Headers.md`
- `Credentialed CORS Requests.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Подтвердить `domain: web-platform`.
2. Подтвердить `section: web-origin-model`.
3. Решить, нужен ли отдельный `section: cors` или достаточно одного общего `section`.
4. Наполнить `CORS` и `Same-Origin Policy` так, чтобы границы между ними были явно различимы.
