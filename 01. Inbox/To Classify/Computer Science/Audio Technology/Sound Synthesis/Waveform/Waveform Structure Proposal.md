---
aliases:
  - Waveform Branch Proposal
note_type: article
area: computer-science
domain: audio-technology
section: sound-synthesis
parent: "[[Waveform]]"
status: draft
related:
  - "[[Waveform]]"
  - "[[Audio-Rate Waveform]]"
  - "[[Control-Rate Waveform]]"
  - "[[Sound Synthesis]]"
tags: []
---

# Waveform Structure Proposal

## Краткая идея ветки

`Waveform` не стоит держать как одну содержательную статью, потому что внутри синтеза звука этот термин покрывает по меньшей мере два разных режима рассмотрения сигнала: слышимый `audio-rate` уровень и управляющий `control-rate` уровень.

## Почему нужен обзорный узел

- Один и тот же термин используется в обоих контекстах, поэтому полезна единая точка входа.
- При этом сами объяснения не стоит смешивать, потому что causal role у этих signal shapes разная.
- Overview-заметка помогает не потерять общее абстрактное ядро и сразу направляет читателя к нужному уровню.

## Предлагаемая структура

- `[[Waveform]]`
- `[[Audio-Rate Waveform]]`
- `[[Control-Rate Waveform]]`

## Роли заметок

- `Waveform` держит только общую рамку и различение уровней.
- `Audio-Rate Waveform` описывает форму слышимого сигнала в контексте oscillators, harmonics, spectrum и timbre.
- `Control-Rate Waveform` описывает форму управляющего сигнала в контексте LFO, envelopes, modulation curves и automation-like control.

## Граница с соседними темами

- `[[Wavetable Synthesis]]` естественно связывается в первую очередь с `[[Audio-Rate Waveform]]`, а не с неразличенным общим `Waveform`.
- `Control-Rate Waveform` пока допустимо держать в этой ветке, но при росте знаний его можно перенести в более широкую ветку modulation или control signals.

## Что стоит раскрыть дальше

- [ ] Решить, когда создавать отдельный узел `Modulation`
- [ ] Проверить, нужны ли отдельные статьи `LFO Shape` и `Envelope Shape`
- [ ] Проверить, нужен ли article для `Single-Cycle Waveform`
