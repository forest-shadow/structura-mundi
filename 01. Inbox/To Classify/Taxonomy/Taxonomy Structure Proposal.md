---
aliases:
  - Taxonomy Structure Proposal
  - Структура ветки Taxonomy
note_type: article
area: computer-science
domain: knowledge-organization
section: taxonomy
parent:
status: draft
related:
  - "[[Taxonomy]]"
  - "[[Hierarchical Classification]]"
  - "[[Faceted Classification]]"
  - "[[Taxonomy and Ontology]]"
tags: []
---

# Taxonomy Structure Proposal

## Краткое определение

Предлагаемая ветка для `Taxonomy` оформляет таксономию как обзорный узел в контексте организации знаний и раскладывает вокруг него устойчивые аспекты: иерархичность, фасетность и границы с близкими моделями.

## Выбранная оптика

- `area: computer-science`
- `domain: knowledge-organization` (предлагаемое новое значение)
- `section: taxonomy` (предлагаемое новое значение)

Почему так:

- в текущем контексте vault тема естественно относится к организации и моделированию знания;
- существующие `domain` из `Corpus Mundi` не дают достаточно точной оптики для этой серии заметок;
- новый `domain` нужен не для одной статьи, а для потенциальной ветки про taxonomy, ontology, classification systems и related knowledge structures.

## Каноническое имя

- корневая заметка: `Taxonomy`
- `Таксономия` лучше хранить в `aliases`

## Рекомендуемая иерархия

```text
Taxonomy
├── Hierarchical Classification
├── Faceted Classification
├── Taxonomy and Ontology
└── Taxonomy and Folksonomy
```

## Почему структура именно такая

- `Taxonomy` лучше сделать `overview`, потому что тема распадается не на один термин, а на несколько устойчивых аспектов.
- `Hierarchical Classification` нужен как статья про базовую форму таксономии.
- `Faceted Classification` нужен как соседняя модель классификации, полезная для сравнения и границ темы.
- `Taxonomy and Ontology` и `Taxonomy and Folksonomy` полезны как статьи-разграничения, потому что именно там чаще всего возникает путаница.

## Что не стоит делать сейчас

- Не стоит сразу добавлять промежуточный overview вроде `Knowledge Organization`, если под ним пока нет корпуса самостоятельных sibling-веток.
- Не стоит создавать отдельные статьи про каждый возможный таксономический узел, ранг или уровень без реального корпуса.
- Не стоит дублировать системный документ `Controlled Vocabulary` отдельной заметкой с тем же именем только ради симметрии.

## Предлагаемое физическое размещение в Corpus Mundi

```text
02. Corpus Mundi/
├── F/
│   └── Faceted Classification.md
├── H/
│   └── Hierarchical Classification.md
└── T/
    ├── Taxonomy.md
    ├── Taxonomy and Folksonomy.md
    └── Taxonomy and Ontology.md
```

## Что уже создано в Inbox

- `[[Taxonomy]]`
- `[[Hierarchical Classification]]`
- `[[Faceted Classification]]`
- `[[Taxonomy and Ontology]]`
- `[[Taxonomy and Folksonomy]]`

## Что стоит раскрыть дальше

- [ ] Уточнить, нужен ли отдельный узел `Knowledge Organization`
- [ ] Проверить, нужна ли отдельная статья про classification scheme
- [ ] Подтвердить `domain: knowledge-organization`
- [ ] Подтвердить `section: taxonomy`
