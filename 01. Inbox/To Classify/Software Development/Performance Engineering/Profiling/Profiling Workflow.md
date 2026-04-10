---
aliases: []
note_type: article
area: computer-science
domain: software-development
section: performance-engineering
parent: "[[Profiling]]"
status: seed
related:
  - "[[Profiling]]"
  - "[[Profiling Targets and Signals]]"
  - "[[Profiling Overhead and Limits]]"
  - "[[Go pprof Analysis Workflow]]"
tags: []
---

# Profiling Workflow

`Profiling Workflow` - это заметка о практическом цикле работы с профилями: сформулировать гипотезу, собрать профиль на релевантной нагрузке, локализовать горячий путь, проверить интерпретацию и только потом менять код.

## Базовый цикл

1. Сформулировать performance question.
2. Выбрать сигнал и способ сбора.
3. Собрать профиль на воспроизводимом сценарии.
4. Прочитать hotspot-ы и call paths.
5. Проверить, что интерпретация не искажена шумом и overhead.
6. Внести изменение и повторно измерить результат.
