# Virtual Memory Structure Proposal

## Назначение

Этот файл фиксирует минимальную иерархию заметок для темы `Virtual Memory` внутри более широкой ветки `Operating Systems`, в которую естественно помещается рассмотрение понятия `OS Virtual Memory`, по правилам `Principia Rerum`.

Для этой ветки нужна предметная рамка:

- `area: computer-science`
- `domain: operating-systems`
- `section: memory-management`

Тема плохо ложится в соседние `domain`, потому что речь идёт не о system design, не о programming languages и не об algorithms, а о внутренней модели работы операционной системы.

## Каноническое имя

- корневая заметка: `Virtual Memory`

`OS Virtual Memory` и `Operating System Virtual Memory` лучше хранить в `aliases`, а не в отдельных заметках.

## Рекомендуемая иерархия

```text
Operating Systems
└── Virtual Memory
    ├── Virtual Address Space
    └── Paging
        ├── Page Table
        ├── TLB
        └── Page Fault
```

## Почему структура именно такая

- `Virtual Memory` оправдан как дочерний `sub-overview` внутри `Operating Systems`, потому что это не одна точка знания, а связанная ветка про адресное пространство, механизм отображения адресов и поведение системы при обращении к отсутствующей странице.
- `Paging` оправдан как вложенный `sub-overview`, потому что внутри него уже есть несколько устойчивых дочерних тем: `Page Table`, `TLB`, `Page Fault`.
- `Virtual Address Space` лучше держать отдельной `article` прямо под `Virtual Memory`, потому что это более общий концептуальный объект, а не подмеханизм paging pipeline.
- Ветка остаётся минимально вложенной и не требует дополнительного промежуточного уровня.

## Текущая физическая раскладка в Inbox

```text
Virtual Memory/
├── Virtual Memory.md
├── Virtual Memory Structure Proposal.md
├── Virtual Address Space.md
└── Paging/
    ├── Paging.md
    ├── Page Table.md
    ├── TLB.md
    └── Page Fault.md
```

## Что не стоит создавать заранее

- `Segmentation`
- `Demand Paging`
- `Swap Space`
- `Memory-Mapped Files`
- `Copy-on-Write`
- `Huge Pages`
- `Memory Management Unit`

Эти темы разумнее сначала раскрывать как разделы внутри уже созданных заметок. Отдельные canonical articles для них нужны только при появлении устойчивого корпуса.

## Предлагаемое физическое размещение после переноса в Corpus Mundi

Если ветка будет доведена до канонического состояния, физическое размещение в `Corpus Mundi` должно следовать алфавитному правилу:

```text
02. Corpus Mundi/
├── P/
│   ├── Page Fault.md
│   ├── Page Table.md
│   └── Paging.md
├── T/
│   └── TLB.md
└── V/
    ├── Virtual Address Space.md
    └── Virtual Memory.md
```

Логическая ветка при этом собирается через `parent`, а не через физическое соседство файлов.

## Что создано в Inbox

- `[[Virtual Memory]]`
- `[[Virtual Address Space]]`
- `[[Paging]]`
- `[[Page Table]]`
- `[[TLB]]`
- `[[Page Fault]]`

## Следующий шаг перед переносом в Corpus Mundi

1. Подтвердить `domain: operating-systems`.
2. Подтвердить `section: memory-management`.
3. Наполнить `Virtual Memory` и `Paging` так, чтобы уже из обзорных узлов было видно различие между общей моделью и конкретным механизмом страничной адресации.
4. Согласовать эту ветку с корневым `[[Operating Systems]]`.
