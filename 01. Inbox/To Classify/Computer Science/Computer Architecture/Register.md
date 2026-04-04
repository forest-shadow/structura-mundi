---
aliases:
  - CPU Register
  - Processor Register
  - Architectural Register
  - Регистр процессора
note_type: article
area: computer-science
domain: computer-architecture
section: instruction-set-architecture
parent: "[[Instruction Set Architecture]]"
status: seed
related:
  - "[[Computer Architecture]]"
  - "[[Instruction Set Architecture]]"
  - "[[Machine Code]]"
  - "[[Compilation]]"
tags: []
---

# Register

## Краткое определение

`Register` — это именованная ячейка или элемент архитектурного состояния процессора, к которому инструкции CPU могут обращаться напрямую по правилам конкретной ISA.

В контексте hardware и CPU регистры образуют ближайший к вычислению слой хранения: именно через них процессор принимает операнды, сохраняет промежуточные результаты, удерживает управляющее состояние и делает часть своего состояния программно наблюдаемой.

## Основная идея или механизм

- регистр предоставляет процессору очень быстро доступное состояние, используемое в ходе исполнения инструкций;
- ISA задает, какие именно регистры существуют, как они именуются и какие операции над ними разрешены;
- значение регистра может участвовать в арифметике, адресации памяти, управлении потоком исполнения и системных переходах;
- регистровая модель определяет важную часть границы между software stack и CPU.

## Границы темы

- Входит: architectural registers, programmer-visible register state, general-purpose и special-purpose registers, связь регистра с instruction semantics.
- Близко, но не совпадает: `Register File` как массив или организация хранения регистров; `physical registers` в out-of-order microarchitecture; `register allocation` как задача компилятора; pipeline registers как внутреннее состояние реализации.

## Связи с другими заметками

Родительская тема:

`[[Instruction Set Architecture]]`

Связанные заметки:

- `[[Computer Architecture]]`
- `[[Instruction Set Architecture]]`
- `[[Machine Code]]`
- `[[Compilation]]`

## Примеры, случаи или следствия

- регистры общего назначения используются как основные операнды арифметических и логических инструкций;
- `Program Counter` удерживает позицию следующей исполняемой инструкции;
- flags, status и control registers участвуют в ветвлениях, обработке исключений, режимах привилегий и системном управлении;
- число и устройство архитектурных регистров прямо влияют на стиль ISA, плотность машинного кода и стратегию компилятора.

## Что стоит раскрыть дальше

- [ ] Развести architectural register и physical register
- [ ] Уточнить связь между `Register` и `Register File`
- [ ] Добавить различие между general-purpose, special-purpose и control/status registers
- [ ] Проверить связь с `Program Counter`, flags и privilege state
- [ ] Проверить `aliases`
