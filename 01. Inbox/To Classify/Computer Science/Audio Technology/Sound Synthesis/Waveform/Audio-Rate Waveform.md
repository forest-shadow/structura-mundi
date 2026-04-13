---
aliases:
  - Audible Waveform
  - Audio Signal Waveform
  - Аудиочастотная форма волны
note_type: article
area: computer-science
domain: audio-technology
section: sound-synthesis
parent: "[[Waveform]]"
status: seed
related:
  - "[[Waveform]]"
  - "[[Sound Synthesis]]"
  - "[[Wavetable Synthesis]]"
  - "[[Wavetable]]"
tags: []
---

# Audio-Rate Waveform

## Краткое определение

`Audio-Rate Waveform` — это waveform слышимого сигнала, работающего на аудиочастотном уровне и потому непосредственно влияющего на спектральный состав, тембр и характер воспринимаемого звука.

## Основная идея или механизм

Когда waveform существует на audio-rate уровне, она выступает материалом самого звука, а не только управляющей кривой. Различие между sine, sawtooth, square и другими формами здесь выражается в различии harmonics и, следовательно, в различии слышимого тембра.

## Границы темы

- В тему входит waveform как форма самого звучащего сигнала.
- С этой темой тесно связаны `Oscillator`, `Spectrum`, `Timbre` и частные family-level waveforms.
- Не стоит смешивать ее с `[[Control-Rate Waveform]]`, где форма сигнала прежде всего управляет параметрами, а не задает слышимую основу звука.

## Связи с другими заметками

Родительская тема:

`[[Waveform]]`

Связанные заметки:

- `[[Sound Synthesis]]`
- `[[Wavetable Synthesis]]`
- `[[Wavetable]]`

## Примеры, случаи или следствия

- Синусоидальная waveform дает наиболее простой спектральный случай и часто служит базовой точкой сравнения.
- Пилообразная waveform содержит богатый набор harmonics и потому часто используется как насыщенный исходный материал.
- В `[[Wavetable Synthesis]]` audio-rate waveforms могут быть организованы в `[[Wavetable]]`, по которому осциллятор перемещается для изменения тембра.

## Что стоит раскрыть дальше

- [ ] Добавить family-level статьи для `Sine Wave`, `Sawtooth Wave` и `Square Wave`
- [ ] Уточнить границу между `Audio-Rate Waveform` и `Single-Cycle Waveform`
- [ ] Проверить, когда нужен отдельный переход к `Spectrum`
