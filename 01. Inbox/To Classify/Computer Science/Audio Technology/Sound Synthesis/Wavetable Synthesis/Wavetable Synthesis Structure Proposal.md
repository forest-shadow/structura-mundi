---
aliases:
  - Wavetable Synthesis Branch Proposal
note_type: article
area: computer-science
domain: audio-technology
section: sound-synthesis
parent: "[[Sound Synthesis]]"
status: draft
related:
  - "[[Sound Synthesis]]"
  - "[[Wavetable Synthesis]]"
  - "[[Wavetable]]"
  - "[[Wavetable Oscillator]]"
  - "[[Waveform]]"
tags: []
---

# Wavetable Synthesis Structure Proposal

## Краткая идея ветки

`Wavetable Synthesis` лучше размещать как локальную overview-ветку внутри `[[Sound Synthesis]]`, потому что это не просто один термин, а компактный кластер тесно связанных понятий: сам метод, таблица волн как источник данных и осциллятор, который эту таблицу читает.

## Почему не отдельная изолированная статья

- Если оставить только одну статью `Wavetable Synthesis`, в ней быстро смешаются метод, структура данных и устройство генератора сигнала.
- Для этой темы естественно разделяются как минимум три уровня: общий метод, `Wavetable` как организованный набор waveforms и `Wavetable Oscillator` как механизм чтения и сканирования таблицы.
- Такая локальная ветка хорошо согласуется с Principia rerum: обзорный узел держит границы темы, а дочерние статьи забирают более узкие сущности.

## Предлагаемая структура

- `[[Sound Synthesis]]`
- `[[Wavetable Synthesis]]`
- `[[Wavetable]]`
- `[[Wavetable Oscillator]]`

## Роли заметок

- `Wavetable Synthesis` стоит держать как overview, где задаются границы метода, ключевая логика изменения тембра и маршрут к дочерним сущностям.
- `Wavetable` стоит держать как article о самой таблице или банке одноцикловых форм волны, используемых как источник сигнала.
- `Wavetable Oscillator` стоит держать как article о генераторе, который выбирает, сканирует и интерполирует позиции внутри wavetable.

## Граница с соседними темами

- `[[Waveform]]` остается более общим понятием о форме сигнала.
- `[[Wavetable]]` уже уже и конкретнее: это не любая форма волны, а упорядоченный набор waveforms, пригодный для чтения в wavetable-based synthesis.
- Если позже понадобится расширение в сторону `Interpolation`, `Morphing` или конкретных synth architectures, их можно будет добавлять только по мере реальной необходимости.

## Что стоит раскрыть дальше

- [ ] Уточнить, считать ли `Wavetable` самостоятельной сущностью вне синтеза или держать его только в synthesis context
- [ ] Решить, когда нужен отдельный article для `Wavetable Position`
- [ ] Проверить, нужен ли переход к более общему `Oscillator`
