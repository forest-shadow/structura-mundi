---
aliases:
  - Modulation Waveform
  - Control Signal Shape
  - Форма управляющего сигнала
note_type: article
area: computer-science
domain: audio-technology
section: sound-synthesis
parent: "[[Waveform]]"
status: seed
related:
  - "[[Waveform]]"
  - "[[Sound Synthesis]]"
tags: []
---

# Control-Rate Waveform

## Краткое определение

`Control-Rate Waveform` — это waveform управляющего сигнала, который используется для изменения параметров во времени и не обязан быть самостоятельным слышимым звуком.

## Основная идея или механизм

На control-rate уровне форма сигнала важна не как источник тембра, а как способ организовать движение параметра. Один и тот же контур может, например, плавно менять cutoff, шагами сдвигать pitch или циклически модулировать amplitude, и именно shape этого сигнала определяет характер изменения.

## Границы темы

- В тему входит waveform как форма modulation или control signal.
- Близки, но не совпадают с этой темой `LFO`, `Envelope`, automation-like curves и другие control sources.
- Не стоит смешивать эту тему с `[[Audio-Rate Waveform]]`, где форма сигнала сама является слышимым материалом.

## Связи с другими заметками

Родительская тема:

`[[Waveform]]`

Связанные заметки:

- `[[Sound Synthesis]]`

## Примеры, случаи или следствия

- Треугольная control-rate waveform может давать плавное периодическое изменение параметра.
- Импульсная или ступенчатая форма может создавать более резкое, дискретное поведение модуляции.
- Даже если control-rate waveform сама по себе не слышна как отдельный tone source, она сильно влияет на воспринимаемую динамику и движение звука.

## Что стоит раскрыть дальше

- [ ] Решить, когда выносить тему в отдельную ветку modulation
- [ ] Проверить, нужны ли отдельные статьи для `LFO Shape` и `Envelope Shape`
- [ ] Уточнить границу между control-rate и sample-and-hold style modulation
