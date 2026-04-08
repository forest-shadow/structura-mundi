# Web Origin Model Structure Proposal

## Назначение

Этот файл фиксирует корневую смысловую иерархию для ветки `Web Origin Model` по правилам `Principia Rerum`.

По смыслу здесь важно описывать не одну статью `CORS`, а весь локальный кластер browser security model, внутри которого `CORS` выступает только одной из составляющих наряду с `origin` и `same-origin policy`.

Используемые значения словаря:

- `area: computer-science`
- `domain: web-platform`
- `section: web-origin-model`

`Web Origin Model` нужен как локальный `overview`, потому что:

- `Web Origin` задаёт базовый объект сравнения;
- `Same-Origin Policy` задаёт исходное ограничение браузера;
- `CORS (Cross-Origin Resource Sharing)` выступает как строго контролируемое ослабление этой модели, а не как самостоятельный корень.

## Рекомендуемая иерархия

```text
Web Origin Model (overview)
├── Web Origin (article)
├── Same-Origin Policy (article)
└── CORS (Cross-Origin Resource Sharing) (article)
```

## Почему структура именно такая

- `Web Origin Model` даёт правильную верхнеуровневую рамку для origin-based ограничений браузера.
- `Web Origin` нужен как отдельная статья, потому что без него вся ветка быстро превращается в набор частных browser rules без базовой сущности сравнения.
- `Same-Origin Policy` следует держать рядом как самостоятельную каноническую статью, потому что именно она задаёт исходный режим запрета, относительно которого потом объясняется `CORS`.
- `CORS (Cross-Origin Resource Sharing)` лучше держать обычной `article`, а не отдельным `sub-overview`, потому что preflight, request headers, response headers и credentialed requests пока выглядят как разделы одной сильной статьи, а не как самостоятельные canonical notes.
- `CORS` здесь должен читаться как составная часть `Web Origin Model`, а не как родительская рамка для всей ветки.
- Если тема действительно вырастет, первым кандидатом на отдельную статью должен быть `Preflight Request`, потому что это самостоятельный механизм внутри `CORS`, а не внутри всей origin-model ветки.

## Что не нужно создавать заранее

Пока не стоит заводить отдельные заметки:

- `Preflight Request`, если заметка дублирует раздел внутри `CORS (Cross-Origin Resource Sharing)`, а не раскрывает самостоятельный механизм;
- отдельные статьи на `CORS Request Headers` и `CORS Response Headers`, если они остаются просто двумя техническими срезами одной схемы обмена;
- отдельную статью на `Credentialed CORS Requests`, если это пока всего лишь режим внутри общей статьи `CORS`;
- отдельные статьи на каждый CORS-заголовок;
- дополнительный промежуточный `overview` между `Web Origin Model` и `CORS`.

Эти узлы можно добавить позже, если статья `CORS` станет перегруженной и внутри неё появятся реально самостоятельные кластеры.

## Предлагаемое физическое размещение после нормализации

Если словарь будет расширен и заметки дойдут до канонического состояния, физическое размещение должно следовать алфавитному правилу:

```text
02. Corpus Mundi/
├── C/
│   └── CORS (Cross-Origin Resource Sharing).md
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
- `CORS (Cross-Origin Resource Sharing).md`

## Следующий шаг перед переносом в Corpus Mundi

1. Подтвердить `domain: web-platform`.
2. Подтвердить `section: web-origin-model`.
3. Не вводить отдельный `section: cors`, пока для него нет устойчивой самостоятельной подветки.
4. Создать или синхронизировать `Web Origin Model.md` как реальный корневой `overview` для этой ветки.
5. Наполнить `CORS (Cross-Origin Resource Sharing)` и `Same-Origin Policy` так, чтобы границы между ними были явно различимы.
