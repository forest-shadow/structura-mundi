# JavaScript Closure Structure Proposal

## Назначение

Этот файл фиксирует подветку `JavaScript Scope Model` для темы `JavaScript Closure` по правилам `Principia Rerum`.

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

- `JavaScript Closure` не стоит держать полностью изолированно, потому что тема напрямую зависит от lexical scope.
- `JavaScript Scope Model` оправдан как минимальный `overview`, который собирает под одной рамкой scope, resolution и closure.
- `Lexical Scope` и `Scope Chain` заслуживают отдельных статей, потому что это устойчивые объекты знания, а не просто подпункты определения closure.
- Более мелкие темы вроде environment records или closure pitfalls пока не нужно выносить в отдельные заметки без плотного корпуса.

## Следующий шаг перед переносом в Corpus Mundi

1. Проверить, не требуется ли позже отдельная статья про `Execution Context`.
2. Наполнить заметки содержанием и развести границы между scope, chain и closure.
