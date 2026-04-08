# JavaScript Scope Model Structure Proposal

## Назначение

Этот файл фиксирует локальную иерархию для ветки `JavaScript Scope Model` по правилам `Principia Rerum`.

По смыслу здесь важно описывать не одну статью `JavaScript Closure`, а весь устойчивый кластер тем про область видимости, разрешение имен и возникновение closure внутри JavaScript.

Для этой ветки подходит уже подтвержденная словарная рамка:

- `area: computer-science`
- `domain: programming-languages`
- `section: javascript`

## Рекомендуемая иерархия

```text
JavaScript (overview)
└── JavaScript Scope Model (overview)
    ├── Lexical Scope (article)
    ├── Scope Chain (article)
    └── JavaScript Closure (article)
```

## Почему структура именно такая

- `JavaScript Scope Model` оправдан как локальный `overview`, который собирает под одной рамкой scope, name resolution и closure.
- `JavaScript Closure` не стоит держать полностью изолированно или делать смысловым корнем этой ветки, потому что closure является следствием scope model, а не более широкой рамкой для нее.
- `Lexical Scope` и `Scope Chain` заслуживают отдельных статей, потому что это устойчивые объекты знания, а не просто подпункты определения closure.
- `JavaScript Closure` корректнее держать обычной `article`, потому что сейчас это один сильный механизм внутри scope model, а не отдельный `sub-overview`.
- Более мелкие темы вроде environment records, variable environment, execution context internals или closure pitfalls пока не нужно выносить в отдельные заметки без плотного корпуса.

## Что не нужно создавать заранее

Пока не стоит заводить отдельные заметки:

- `Execution Context`, если он пока нужен только как соседняя объясняющая рамка, а не как уже устойчивый самостоятельный кластер;
- `Environment Record`, если материал пока естественно раскрывается внутри `Lexical Scope` или `JavaScript Closure`;
- `Closure Pitfalls` как отдельную каноническую статью, если это пока всего лишь прикладной раздел внутри `JavaScript Closure`;
- дополнительный промежуточный `overview` между `JavaScript Scope Model` и `JavaScript Closure`.

## Предлагаемое физическое размещение после нормализации

Если заметки будут доведены до канонического состояния, физическое размещение должно следовать алфавитному правилу:

```text
02. Corpus Mundi/
├── J/
│   ├── JavaScript Scope Model.md
│   └── JavaScript Closure.md
├── L/
│   └── Lexical Scope.md
└── S/
    └── Scope Chain.md
```

Логическая ветка при этом всё равно собирается через `parent`.

## Созданные черновые заметки

- `JavaScript Scope Model.md`
- `Lexical Scope.md`
- `Scope Chain.md`
- `JavaScript Closure.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Проверить, не требуется ли позже отдельная статья про `Execution Context`.
2. Синхронизировать формулировки в `JavaScript Scope Model.md`, чтобы closure явно читался как следствие scope model.
3. Наполнить заметки содержанием и развести границы между scope, chain и closure.
