# Syllogism Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для темы `Syllogism` по правилам `Principia Rerum`.

Ветка пока размещена в `Inbox`, потому что для нее требуется расширение управляемого словаря:

- `area: philosophy`
- `domain: logic` (предлагаемое новое значение)
- `section: syllogistics` (предлагаемое новое значение)

До фиксации этих значений в `Controlled Vocabulary` ветку не стоит считать готовой к переносу в `02. Corpus Mundi`.

## Рекомендуемая иерархия

```text
Syllogism (overview)
├── Categorical Syllogism (overview)
│   ├── Syllogistic Figure (article)
│   └── Syllogistic Mood (article)
├── Hypothetical Syllogism (article)
└── Disjunctive Syllogism (article)
```

## Почему структура именно такая

- `Syllogism` является естественной канонической обзорной точкой входа для всей ветки.
- Один вложенный `overview` для `Categorical Syllogism` оправдан, потому что именно внутри этой темы появляются собственные устойчивые оси рассмотрения: `Figure` и `Mood`.
- `Hypothetical Syllogism` и `Disjunctive Syllogism` пока лучше держать как обычные `article`, а не разворачивать в отдельные обзорные ветки без накопленного корпуса.
- Глубже одного вложенного `overview` идти не нужно, если не появится отдельный насыщенный корпус заметок.

## Что не нужно создавать заранее

Пока не стоит заводить отдельные узлы:

- `Logic` как обзорную ветку только ради размещения `Syllogism`;
- `Deductive Inference` как промежуточный слой;
- отдельные заметки для `Major Term`, `Minor Term`, `Middle Term`, `Major Premise`, `Minor Premise`, `Conclusion`, если по ним еще нет самостоятельного материала.

Эти сущности можно добавить позже как `article`, если ветка реально вырастет.

## Предлагаемое физическое размещение после нормализации

Если словарь будет расширен и заметки дойдут до канонического состояния, их физическое размещение должно следовать алфавитному правилу:

```text
02. Corpus Mundi/
├── C/
│   └── Categorical Syllogism.md
├── D/
│   └── Disjunctive Syllogism.md
├── H/
│   └── Hypothetical Syllogism.md
└── S/
    ├── Syllogism.md
    ├── Syllogistic Figure.md
    └── Syllogistic Mood.md
```

Локальные вложения при необходимости:

```text
02. Corpus Mundi/S/_resources/Syllogism/
```

## Созданные черновые заметки

- `Syllogism.md`
- `Categorical Syllogism.md`
- `Hypothetical Syllogism.md`
- `Disjunctive Syllogism.md`
- `Syllogistic Figure.md`
- `Syllogistic Mood.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Подтвердить `domain: logic`.
2. Подтвердить `section: syllogistics`.
3. Решить, остается ли каноническое имя на английском (`Syllogism`) с русским `alias`, или для философского корпуса нужен другой языковой стандарт.
4. После этого перевести заметки из `seed` в рабочие черновики и наполнить содержанием.
