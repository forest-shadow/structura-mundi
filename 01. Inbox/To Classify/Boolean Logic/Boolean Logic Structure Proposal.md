# Boolean Logic Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для темы `Boolean Logic`, в которую естественно помещается рассмотрение булевых значений, таблиц истинности и логических связок, по правилам `Principia Rerum`.

Ветка пока должна жить в `Inbox`, потому что для нее предлагается новое значение управляемого словаря:

- `area: philosophy`
- `domain: logic`
- `section: boolean-logic` (предлагаемое новое значение)

Новый `domain` не нужен: тема естественно встраивается в уже существующий `domain: logic`. До фиксации `section: boolean-logic` в `Controlled Vocabulary` ветку не стоит считать готовой к переносу в `02. Corpus Mundi`.

## Рекомендуемая иерархия

```text
Boolean Logic (overview)
├── Logical Connectives (overview)
│   ├── Logical Negation (article)
│   ├── Logical Conjunction (article)
│   ├── Logical Disjunction (article)
│   ├── Logical Implication (article)
│   └── Logical Equivalence (article)
├── Truth Value (article)
└── Truth Table (article)
```

## Почему структура именно такая

- `Boolean Logic` нужен как корневой `overview`, потому что тема уже собирает не один частный механизм, а устойчивую локальную ветку формальной логики.
- `Logical Connectives` оправдан как вложенный `overview`, потому что именно вокруг связок естественно группируются несколько самостоятельных notes: отрицание, конъюнкция, дизъюнкция, импликация и эквиваленция.
- `Truth Value` лучше держать отдельной `article`, потому что это базовое понятие ветки, но пока не отдельный обзорный кластер.
- `Truth Table` тоже корректнее держать отдельной `article`, потому что это универсальный метод представления истинностных зависимостей, а не подветка с собственной глубокой иерархией.
- Глубже одного вложенного `overview` идти не стоит, пока не накопится отдельный корпус заметок, например про normal forms, logical equivalence laws или proof systems.

## Что не стоит создавать заранее

- отдельную обзорную заметку `Logic` только ради размещения `Boolean Logic`, потому что сейчас это создаст лишний промежуточный слой;
- отдельную заметку `Propositional Logic`, если она будет просто дублировать `Boolean Logic` под другим именем;
- отдельные заметки под `AND`, `OR`, `NOT` как чисто символические варианты без самостоятельного содержания поверх канонических `Logical Conjunction`, `Logical Disjunction` и `Logical Negation`;
- специальные тематические template-файлы под булеву логику, потому что по `Principia Rerum` в vault должны оставаться только канонические `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение после нормализации

Если ветка будет подтверждена и доведена до канонического состояния, физическое размещение должно следовать алфавитному правилу:

```text
02. Corpus Mundi/
├── B/
│   └── Boolean Logic.md
├── L/
│   ├── Logical Connectives.md
│   ├── Logical Conjunction.md
│   ├── Logical Disjunction.md
│   ├── Logical Equivalence.md
│   ├── Logical Implication.md
│   └── Logical Negation.md
└── T/
    ├── Truth Table.md
    └── Truth Value.md
```

Логическая ветка при этом собирается через `parent`, а не через вложенные папки.

## Созданные seed-заготовки

- `Boolean Logic.md`
- `Logical Connectives.md`
- `Logical Negation.md`
- `Logical Conjunction.md`
- `Logical Disjunction.md`
- `Logical Implication.md`
- `Logical Equivalence.md`
- `Truth Value.md`
- `Truth Table.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Подтвердить `section: boolean-logic`.
2. Уточнить, остается ли `Propositional Logic` alias-именем для этой ветки или позже должен стать соседней, но не тождественной заметкой.
3. Решить, нужен ли отдельный article `Boolean Expression`, когда появится больше прикладного материала из computer science.
4. Наполнить `Logical Connectives` и `Truth Table` примерами, чтобы ветка не оставалась чисто номинальной.
