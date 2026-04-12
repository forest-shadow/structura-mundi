---
aliases:
  - File Linking Structure Proposal
note_type: article
area: computer-science
domain: operating-systems
section: linux
parent: "[[Linking Files]]"
status: draft
related:
  - "[[Linux File System]]"
  - "[[Linking Files]]"
  - "[[Inode]]"
  - "[[Hard Link]]"
  - "[[Symbolic Link]]"
  - "[[File Systems]]"
tags: []
---

# Linking Files Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для темы `Linking Files`, в которую естественно помещается рассмотрение hard links и symbolic links в контексте Linux по правилам `Principia Rerum`.

Для этой ветки достаточно уже существующей словарной рамки:

- `area: computer-science`
- `domain: operating-systems`
- `section: linux`

Отдельный `domain` или новый `section` не нужен: file linking здесь выступает как локальный механизм внутри Linux filesystem branch.

## Рекомендуемая иерархия

```text
Operating Systems
└── Linux
    └── Linux File System
        └── Linking Files
            ├── Hard Link
            └── Symbolic Link
```

## Почему структура именно такая

- `Linking Files` лучше сделать `overview`, потому что один родительский узел нужен для сопоставления двух разных форм ссылок без смешения их свойств в одной длинной статье.
- `Inode` не стоит подвешивать внутрь `Linking Files`: это более широкая Linux filesystem-сущность, которая нужна не только для hard links, но и для общей модели file object identity.
- `Hard Link` остаётся обычной `article`, потому что это конкретный механизм дополнительного имени для того же filesystem object.
- `Symbolic Link` тоже остаётся обычной `article`, потому что это другой конкретный механизм, основанный на ссылке по пути, а не на разделении того же файлового объекта.
- Не стоит делать отдельную каноническую статью `Soft Link`: в Linux инженерной нормой является `Symbolic Link`, а `Soft Link` лучше хранить в `aliases`.

## Что не стоит создавать заранее

- отдельную каноническую заметку `Soft Link`, если она будет дублировать `Symbolic Link`;
- отдельные статьи только под команды `ln` и `ln -s`, пока речь идёт о понятийной ветке, а не о справочнике утилит;
- отдельный `overview` про `inode semantics`, если уже созданная статья `Inode` покрывает нужную гранулярность;
- специальные template-файлы под file-linking branch, потому что по `Principia Rerum` в системе должны оставаться только общие канонические шаблоны.

## Текущая физическая раскладка в Inbox

```text
01. Inbox/To Classify/Operating Systems/Linux/Linux File System/Linking Files/
├── Linking Files.md
├── Linking Files Structure Proposal.md
├── Hard Link.md
└── Symbolic Link.md
```

## Предлагаемое физическое размещение после нормализации

После нормализации в `02. Corpus Mundi` эти заметки должны раскладываться по алфавитному индексному написанию, а логическая связность ветки должна удерживаться через `parent`.

## Созданные seed-заготовки

- `[[Linking Files]]`
- `[[Hard Link]]`
- `[[Symbolic Link]]`

## Следующий шаг перед переносом в Corpus Mundi

1. Уточнить формулировку различия между same inode и path-based reference.
2. Согласовать `Linking Files` с отдельной статьей `[[Inode]]`, чтобы hard-link semantics не дублировалась в двух местах.
3. Добавить практические Linux consequences для удаления, переименования и пересечения filesystem boundaries.
4. Проверить `aliases` у `Symbolic Link`, чтобы `Soft Link` жил именно там.
