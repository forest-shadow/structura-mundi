---
aliases:
  - ALU
  - Арифметико-логическое устройство
note_type: article
area: computer-science
domain: computer-architecture
section: microarchitecture
parent: "[[Microarchitecture]]"
status: seed
related:
  - "[[Computer Architecture]]"
  - "[[Microarchitecture]]"
  - "[[Instruction Set Architecture]]"
tags: []
---

# Arithmetic Logic Unit

## Краткое определение

`Arithmetic Logic Unit` — это вычислительный блок процессора, который выполняет базовые арифметические и логические операции над операндами, поступающими из регистров, immediate-значений или других внутренних путей datapath.

## Основная идея или механизм

ALU является частью внутренней реализации процессора, а не программно-видимой спецификации ISA. Именно через такие блоки процессор физически реализует сложение, вычитание, сравнение, побитовые операции, вычисление адресных смещений и другие elementary integer-style transformations, которые затем проявляются на архитектурном уровне как эффект исполнения инструкций.

## Границы темы

- В тему входят integer arithmetic, logical operations, comparisons, flag-affecting behavior и роль ALU внутри execution stage.
- На границе находятся `FPU`, `Vector Unit`, `Control Unit` и вся тема `Instruction Set Architecture`, потому что они либо описывают другие вычислительные блоки, либо другой уровень абстракции.

## Связи с другими заметками

Родительская тема:

`[[Microarchitecture]]`

Связанные заметки:

- `[[Computer Architecture]]`
- `[[Instruction Set Architecture]]`

## Примеры, случаи или следствия

- Даже если ISA описывает инструкцию `ADD`, сама спецификация не требует одной-единственной физической ALU-реализации: разные процессоры могут иметь разные execution pipelines и разное число ALU blocks.
- В простых учебных моделях CPU ALU часто показывается как центральная часть datapath, через которую проходят arithmetic and logical transformations.

## Что стоит раскрыть дальше

- [ ] Уточнить связь ALU с flags, condition codes и compare instructions
- [ ] Добавить границу между ALU, FPU и vector execution units
- [ ] Проверить `aliases`
- [ ] Проверить `related`
