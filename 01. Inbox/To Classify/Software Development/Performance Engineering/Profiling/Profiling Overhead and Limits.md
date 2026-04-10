---
aliases:
  - Profiling Bias and Overhead
note_type: article
area: computer-science
domain: software-development
section: performance-engineering
parent: "[[Profiling]]"
status: seed
related:
  - "[[Profiling]]"
  - "[[Profiling Workflow]]"
  - "[[Performance Modeling]]"
tags: []
---

# Profiling Overhead and Limits

`Profiling Overhead and Limits` - это заметка об ограничениях profiling как метода измерения: сам профайлер вмешивается в систему, может смещать картину исполнения и не отвечает автоматически на вопрос, какое изменение действительно улучшит программу.

## Что важно удерживать

- sampling и instrumentation дают разную степень вмешательства;
- профили без релевантной нагрузки часто создают ложные выводы;
- hotspot не всегда совпадает с самой полезной точкой оптимизации;
- profiling лучше работает в связке с benchmark, domain knowledge и повторным измерением после изменений.
