---
aliases:
  - Compilation Branch Structure Proposal
note_type: article
area: computer-science
domain: programming-languages
section: compilation
parent:
status: seed
related:
  - "[[Compilation]]"
  - "[[Programming Languages]]"
  - "[[Program Translation Pipeline]]"
  - "[[Program Binary Formats]]"
  - "[[Executable Binary]]"
  - "[[Object File]]"
  - "[[Shared Library]]"
tags: []
---

# Compilation Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для темы `Compilation` внутри `Programming Languages` по правилам `Principia Rerum`.

Для этой ветки подходит предметная рамка:

- `area: computer-science`
- `domain: programming-languages`
- `section: compilation`

## Каноническое имя

- корневая обзорная заметка: `Compilation`

Термин `Source Code Execution Pipeline` лучше не делать каноническим именем, потому что он смешивает этапы трансляции с уже последующим исполнением программы. Для узла про последовательность преобразований исходного кода точнее использовать `Program Translation Pipeline`.

## Рекомендуемая иерархия

```text
Programming Languages
└── Compilation
    ├── Program Binary Formats
    │   ├── ELF
    │   └── DWARF
    ├── Program Translation Pipeline
    │   ├── Lexical Analysis
    │   ├── Parsing
    │   ├── Semantic Analysis
    │   ├── Intermediate Representation
    │   ├── Code Generation
    │   └── Linking
    ├── Abstract Syntax Tree
    ├── Machine Code
    ├── Object File
    ├── Shared Library
    └── Executable Binary
```

## Почему структура именно такая

- `Compilation` оправдан как дочерний `overview` внутри `Programming Languages`, потому что тема собирает не одну статью, а устойчивую группу взаимосвязанных заметок про трансляцию программы.
- `Program Translation Pipeline` лучше, чем `Source Code Execution Pipeline`, потому что здесь речь идет именно о преобразовании source code в промежуточные и конечные представления, а не о runtime execution.
- `Program Translation Pipeline` оправдан как вложенный `overview`, потому что внутри него уже есть устойчивый набор стадий: lexical analysis, parsing, semantic analysis, intermediate representation, code generation и linking.
- `Program Binary Formats` оправдан как вложенный `overview`, потому что `ELF` и `DWARF` уже образуют минимальный локальный кластер про конкретные стандартизованные бинарные форматы и форматы debug information.
- `PE` и `Mach-O` не нужно заводить автоматически только ради симметрии с `ELF`. По `Principia Rerum` новый узел нужен тогда, когда он уже становится самостоятельной канонической точкой чтения, а не placeholder-симметрией.
- `Abstract Syntax Tree` лучше держать отдельной статьёй, а не просто разделом внутри `Parsing`, потому что AST выступает самостоятельным представлением программы и используется также в semantic analysis, optimization и code generation.
- `Machine Code` и `Executable Binary` лучше держать отдельными статьями, потому что это не тождественные понятия: machine code — это низкоуровневые инструкции, а executable binary — итоговый артефакт после упаковки и линковки.
- `Object File` и `Shared Library` уже оправданы как отдельные `article`, потому что это не форматы, а устойчивые виды бинарных артефактов. На них естественно ссылаются `Compilation`, `Linking`, `Executable Binary` и `ELF`.
- `ELF` не стоит подвешивать напрямую под `Executable Binary`, потому что по правилам `Principia Rerum` дочерняя заметка должна указывать в `parent` обзорный узел, а `Executable Binary` по текущей модели остается обычной `article`.
- `DWARF` не стоит жестко подчинять только `ELF`, потому что здесь важнее выделить формат debug information как самостоятельную статью рядом с форматом бинарного контейнера.
- Отдельный общий узел `Debugging Symbols` пока преждевременен. Если такой узел позднее понадобится, точнее каноническое имя `Debug Information`, потому что DWARF шире, чем просто symbols.
- Дополнительную глубину пока не стоит вводить через новые обзорные слои: темы вроде `Assembler`, `Bytecode`, `Symbol Table`, `Control Flow Graph` и `Loader` разумнее сначала раскрывать как разделы внутри существующих notes и выносить только при накоплении корпуса.

## Что не стоит создавать заранее

- отдельную корневую ветку `Compiler Theory`, если пока задача ограничена базовой compilation-веткой;
- отдельный `overview` только для `Parsing`, если пока достаточно обычной article-note;
- превращать `Executable Binary` в вынужденный `overview` только ради подвешивания `ELF` и `DWARF`;
- добавлять `PE` и `Mach-O` только потому, что рядом уже есть `ELF`, если в ветке еще нет реального корпуса про межплатформенные бинарные форматы;
- заводить общий узел `Debugging Symbols` до появления второго самостоятельного формата рядом с `DWARF` или достаточного количества материала именно про общую тему debug information;
- специальные тематические template-файлы под compiler notes, потому что по `Principia Rerum` должны оставаться только канонические `Overview Template` и `Article Template`.

## Текущая физическая раскладка в Inbox

```text
Compilation/
├── Compilation Structure Proposal.md
├── Abstract Syntax Tree.md
├── Machine Code.md
├── Object File.md
├── Shared Library.md
├── Executable Binary.md
├── Program Binary Formats/
│   ├── Program Binary Formats.md
│   ├── Program Binary Formats Structure Proposal.md
│   ├── ELF.md
│   └── DWARF.md
└── Program Translation Pipeline/
    ├── Program Translation Pipeline.md
    ├── Lexical Analysis.md
    ├── Parsing.md
    ├── Semantic Analysis.md
    ├── Intermediate Representation.md
    ├── Code Generation.md
    └── Linking.md
```

## Предлагаемое физическое размещение после переноса в Corpus Mundi

Если ветка будет доведена до канонического состояния, её физическое размещение в `Corpus Mundi` должно следовать алфавитному правилу:

```text
02. Corpus Mundi/
├── A/
│   └── Abstract Syntax Tree.md
├── C/
│   ├── Compilation.md
│   └── Code Generation.md
├── D/
│   └── DWARF.md
├── E/
│   ├── ELF.md
│   └── Executable Binary.md
├── I/
│   └── Intermediate Representation.md
├── L/
│   ├── Lexical Analysis.md
│   └── Linking.md
├── M/
│   └── Machine Code.md
├── O/
│   └── Object File.md
├── P/
│   ├── Parsing.md
│   └── Program Translation Pipeline.md
└── S/
    ├── Semantic Analysis.md
    └── Shared Library.md
```

Логическая ветка при этом всё равно собирается через `parent`, а не через физическое соседство файлов.

## Что уже создано в Inbox

- `[[Program Binary Formats]]`
- `[[ELF]]`
- `[[DWARF]]`
- `[[Program Translation Pipeline]]`
- `[[Lexical Analysis]]`
- `[[Parsing]]`
- `[[Abstract Syntax Tree]]`
- `[[Semantic Analysis]]`
- `[[Intermediate Representation]]`
- `[[Code Generation]]`
- `[[Machine Code]]`
- `[[Object File]]`
- `[[Shared Library]]`
- `[[Linking]]`
- `[[Executable Binary]]`

## Следующий шаг перед переносом в Corpus Mundi

1. Подтвердить `section: compilation`.
2. Проверить, не нужен ли позднее более широкий узел `Language Implementation`.
3. Довести `Object File` и `Shared Library` до состояния, в котором уже из самих заметок видно их отличие от `Executable Binary` и от конкретных контейнерных форматов.
4. Возвращаться к `PE` и `Mach-O` только если ветка `Program Binary Formats` действительно станет сравнительной по Unix, Windows и macOS.
5. Возвращаться к общему узлу про debug metadata только когда рядом с `DWARF` появится второй самостоятельный формат или корпус про общую тему `Debug Information`.

# Compilation: Рекомендуемый маршрут чтения

1. Начать с `Compilation`.
2. Затем перейти к `[[Program Translation Pipeline]]`, чтобы увидеть общую последовательность преобразований.
3. После этого читать `[[Abstract Syntax Tree]]`, `[[Machine Code]]`, `[[Object File]]`, `[[Shared Library]]` и `[[Executable Binary]]` как ключевые представления и результаты процесса.

## Как устроена ветка

- `Compilation` служит корневым `overview` для общей темы трансляции программы.
- Отдельный вложенный `overview` `[[Program Translation Pipeline]]` нужен для устойчивого набора стадий вроде lexical analysis, parsing, semantic analysis, code generation и linking.
- Отдельный вложенный `overview` `[[Program Binary Formats]]` нужен для локального кластера конкретных бинарных представлений вроде `[[ELF]]` и `[[DWARF]]`.
- `Abstract Syntax Tree`, `Machine Code`, `Object File`, `Shared Library` и `Executable Binary` лучше держать отдельными `article`, потому что это не просто шаги конвейера, а самостоятельные представления или артефакты, к которым будут вести ссылки из разных частей ветки.

## Что стоит раскрыть дальше

- [ ] Проверить, когда рядом нужны `Compiler`, `Interpreter` и `Linker`
- [ ] Проверить, когда рядом с `Program Binary Formats` действительно нужны `PE` и `Mach-O`
- [ ] Проверить границы между compilation, build pipeline и program execution
