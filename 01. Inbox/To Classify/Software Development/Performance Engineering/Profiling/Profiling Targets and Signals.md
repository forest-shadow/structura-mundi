---
aliases:
  - Profiling Signals
note_type: article
area: computer-science
domain: software-development
section: performance-engineering
parent: "[[Profiling]]"
status: seed
related:
  - "[[Profiling]]"
  - "[[Profiling Workflow]]"
  - "[[Go pprof Profile Types]]"
  - "[[Go pprof]]"
tags: []
---

# Profiling Targets and Signals

`Profiling Targets and Signals` - это заметка о том, какие стороны поведения программы вообще можно профилировать: CPU time, wall-clock latency, allocations, heap growth, lock contention, blocking, I/O wait и похожие сигналы исполнения.

## Что входит

- различие между ресурсом, который измеряется, и инструментом, которым он измеряется;
- различие между sampled и instrumented signals;
- связь между типом сигнала и типом bottleneck.

## Что не входит

- пошаговый workflow чтения профиля;
- language-specific детали конкретных профайлеров.
