---
aliases:
  - Structure-Preserving Mappings Structure Proposal
  - Структура ветки Structure-Preserving Mappings
note_type: article
area: philosophy
domain: logic
section: structure-preserving-mappings
parent:
status: draft
related:
  - "[[Structure-Preserving Mappings]]"
  - "[[Homomorphism]]"
  - "[[Isomorphism]]"
  - "[[Automorphism]]"
tags: []
---

# Structure-Preserving Mappings Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для темы `Structure-Preserving Mappings`, в которую естественно помещается рассмотрение понятия `Isomorphism`, по правилам `Principia Rerum`.

## Выбранная оптика

- `area: philosophy`
- `domain: logic`
- `section: structure-preserving-mappings` (предлагаемое новое значение)

Почему так:

- новый `area: mathematics` здесь нельзя вводить локально, потому что `area` в `Controlled Vocabulary` закрыт и меняется только на уровне правил;
- `domain: logic` уже существует и лучше всего подходит для формального рассмотрения отображений между структурами;
- отдельный `section` оправдан не одной заметкой: рядом с `Isomorphism` естественно возникают `Homomorphism`, `Endomorphism`, `Automorphism`, а позднее при росте корпуса могут появиться `Isomorphism Invariant`, `Graph Isomorphism` и `Order Isomorphism`.

## Рекомендуемая иерархия

```text
Structure-Preserving Mappings (overview)
├── Homomorphism (article)
├── Endomorphism (article)
├── Isomorphism (article)
└── Automorphism (article)
```

## Почему структура именно такая

- `Structure-Preserving Mappings` нужен как корневой `overview`, чтобы `Isomorphism` не висел одиночной статьей без ближайшего смыслового окружения.
- `Homomorphism` лучше держать базовой `article`, потому что именно он задает общий паттерн сохранения операций, отношений или сигнатуры.
- `Isomorphism` естественно размещать рядом как более сильный случай, где сохранение структуры сочетается с обратимостью и позволяет говорить о структурной тождественности объектов.
- `Endomorphism` и `Automorphism` образуют устойчивую пару специальных случаев самодействия структуры на самой себе, поэтому их разумно держать в той же ветке, а не разносить по разным разделам.
- Глубже одного `overview` идти пока не стоит: для отдельного промежуточного узла вроде `Morphisms` или `Structural Equivalence` здесь еще нет достаточного корпуса.

## Что не стоит создавать заранее

- отдельную `Logic` overview-ветку только ради размещения этой темы, потому что это даст лишний промежуточный слой без достаточного числа sibling-веток;
- новый `area: mathematics`, потому что это уже изменение системного словаря, а не локальная раскладка одной ветки;
- отдельную статью `Morphism`, если она будет лишь пустым контейнером между `Structure-Preserving Mappings` и реальными понятиями;
- специальные тематические template-файлы под эту ветку, потому что по `Principia Rerum` здесь должны оставаться только канонические `Overview Template` и `Article Template`.

## Предлагаемое физическое размещение после нормализации

```text
02. Corpus Mundi/
├── A/
│   └── Automorphism.md
├── E/
│   └── Endomorphism.md
├── H/
│   └── Homomorphism.md
├── I/
│   └── Isomorphism.md
└── S/
    └── Structure-Preserving Mappings.md
```

Логическая ветка при этом собирается через `parent`, а не через вложенные директории.

## Созданные seed-заготовки

- `Structure-Preserving Mappings.md`
- `Homomorphism.md`
- `Endomorphism.md`
- `Isomorphism.md`
- `Automorphism.md`

## Следующий шаг перед переносом в Corpus Mundi

1. Подтвердить `section: structure-preserving-mappings`.
2. Решить, остается ли эта ветка в `domain: logic` как основная формальная оптика, если позже в словаре появится отдельный `area: mathematics`.
3. Уточнить, когда рядом с `Isomorphism` нужен отдельный article `Isomorphism Invariant`.
4. Наполнить заметки примерами из алгебры, теории графов и формальной логики, чтобы ветка не оставалась чисто номинальной.
