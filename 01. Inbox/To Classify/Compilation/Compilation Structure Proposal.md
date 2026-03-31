---
aliases:
  - Compilation Branch Structure Proposal
note_type: article
area: computer-science
domain: programming-languages
section: compilation
parent:
status: draft
related:
  - "[[Compilation]]"
  - "[[Programming Languages]]"
  - "[[Program Translation Pipeline]]"
tags: []
---

# Compilation Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для темы `Compilation` внутри `Programming Languages` по правилам `Principia Rerum`.

Для этой ветки подходит предметная рамка:

- `area: computer-science`
- `domain: programming-languages`
- `section: compilation` (новый тематический кластер для compilation-related notes)

## Каноническое имя

- корневая обзорная заметка: `Compilation`

Термин `Source Code Execution Pipeline` лучше не делать каноническим именем, потому что он смешивает этапы трансляции с этапом уже последующего исполнения программы. Для узла про последовательность преобразований исходного кода точнее использовать `Program Translation Pipeline`.

## Рекомендуемая иерархия

```text
Programming Languages
└── Compilation
    ├── Program Translation Pipeline
    │   ├── Lexical Analysis
    │   ├── Parsing
    │   ├── Semantic Analysis
    │   ├── Intermediate Representation
    │   ├── Code Generation
    │   └── Linking
    ├── Abstract Syntax Tree
    ├── Machine Code
    └── Executable Binary
```

## Почему структура именно такая

- `Compilation` оправдан как дочерний `overview` внутри `Programming Languages`, потому что тема собирает не одну статью, а устойчивую группу взаимосвязанных заметок про трансляцию программы.
- `Program Translation Pipeline` лучше, чем `Source Code Execution Pipeline`, потому что здесь речь идет именно о преобразовании source code в промежуточные и конечные представления, а не о runtime execution.
- `Program Translation Pipeline` оправдан как вложенный `overview`, потому что внутри него уже есть устойчивый набор стадий: lexical analysis, parsing, semantic analysis, intermediate representation, code generation и linking.
- `Abstract Syntax Tree` лучше держать отдельной статьей, а не просто разделом внутри `Parsing`, потому что AST выступает самостоятельным представлением программы и используется также в semantic analysis, optimization и code generation.
- `Machine Code` и `Executable Binary` лучше держать отдельными статьями, потому что это не тождественные понятия: machine code — это низкоуровневые инструкции, а executable binary — итоговый артефакт после упаковки и линковки.
- Дополнительную глубину пока не стоит вводить: темы вроде `Assembler`, `Object File`, `Bytecode`, `Symbol Table`, `Control Flow Graph` и `Loader` разумнее сначала раскрывать как разделы внутри существующих notes и выносить только при накоплении корпуса.

## Что не стоит создавать заранее

- отдельную корневую ветку `Compiler Theory`, если пока задача ограничена базовой compilation-веткой;
- отдельный `overview` только для `Parsing`, если пока достаточно обычной article-note;
- специальные тематические template-файлы под compiler notes, потому что по `Principia Rerum` должны оставаться только канонические `Overview Template` и `Article Template`.

## Текущая физическая раскладка в Inbox

```text
Compilation/
├── Compilation.md
├── Compilation Structure Proposal.md
├── Abstract Syntax Tree.md
├── Machine Code.md
├── Executable Binary.md
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
├── E/
│   └── Executable Binary.md
├── I/
│   └── Intermediate Representation.md
├── L/
│   ├── Lexical Analysis.md
│   └── Linking.md
├── M/
│   └── Machine Code.md
├── P/
│   ├── Parsing.md
│   └── Program Translation Pipeline.md
└── S/
    └── Semantic Analysis.md
```

Логическая ветка при этом всё равно собирается через `parent`, а не через физическое соседство файлов.

## Что уже создано в Inbox

- `[[Compilation]]`
- `[[Program Translation Pipeline]]`
- `[[Lexical Analysis]]`
- `[[Parsing]]`
- `[[Abstract Syntax Tree]]`
- `[[Semantic Analysis]]`
- `[[Intermediate Representation]]`
- `[[Code Generation]]`
- `[[Machine Code]]`
- `[[Linking]]`
- `[[Executable Binary]]`

## Следующий шаг перед переносом в Corpus Mundi

1. Подтвердить `section: compilation`.
2. Проверить, не нужен ли позднее более широкий узел `Language Implementation`.
3. Уточнить границы между `Compilation`, `Program Translation Pipeline` и будущими notes про `Interpreter` или `Loader`.
4. Наполнить `Compilation` и `Program Translation Pipeline` так, чтобы уже из overview-узлов было видно различие между стадиями процесса и артефактами процесса.


# Compilation: Рекомендуемый маршрут чтения

1. Начать с `Compilation`.
2. Затем перейти к `[[Program Translation Pipeline]]`, чтобы увидеть общую последовательность преобразований.
3. После этого читать `[[Abstract Syntax Tree]]`, `[[Machine Code]]` и `[[Executable Binary]]` как ключевые представления и результаты процесса.

## Как устроена ветка

- `Compilation` служит корневым `overview` для общей темы трансляции программы.
- Отдельный вложенный `overview` `[[Program Translation Pipeline]]` нужен для устойчивого набора стадий вроде lexical analysis, parsing, semantic analysis, code generation и linking.
- `Abstract Syntax Tree`, `Machine Code` и `Executable Binary` лучше держать отдельными `article`, потому что это не просто шаги конвейера, а самостоятельные представления или артефакты, к которым будут вести ссылки из разных частей ветки.
## Что стоит раскрыть дальше

- [ ] Проверить, когда рядом нужны `Compiler`, `Interpreter` и `Linker`
- [ ] Проверить границы между compilation, build pipeline и program execution