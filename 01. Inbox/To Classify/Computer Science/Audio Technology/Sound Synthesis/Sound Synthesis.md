---
aliases:
  - Audio Synthesis
  - Синтез звука
note_type: overview
area: computer-science
domain: audio-technology
section: sound-synthesis
parent: "[[Audio Technology]]"
status: seed
related:
  - "[[Audio Technology]]"
  - "[[Waveform]]"
  - "[[Wavetable Synthesis]]"
tags: []
---

# Sound Synthesis

## Краткое определение области

`Sound Synthesis` — это section-level overview внутри `audio-technology`, собирающий заметки о способах искусственного порождения и формообразования звука, где ключевую роль играют исходный сигнал, его временная форма, спектральный состав и методы управления изменением тембра во времени.

## Что входит в эту тему

- `[[Waveform]]`
- `[[Wavetable Synthesis]]`

## Как устроена ветка

- `Sound Synthesis` лучше держать как отдельный обзорный узел, потому что здесь естественно группируются не одна, а серия тесно связанных тем.
- `Waveform` лучше держать как overview-узел, который не смешивает разные роли сигнала, а разводит их по дочерним заметкам `Audio-Rate Waveform` и `Control-Rate Waveform`.
- `Wavetable Synthesis` имеет смысл держать как отдельную локальную overview-ветку внутри `Sound Synthesis`, потому что рядом с методом естественно появляются собственные дочерние понятия: `Wavetable` и `Wavetable Oscillator`.
- По мере роста ветки часть control-rate тем может потребовать выноса из `Sound Synthesis` в более общую ветку про modulation или control signals, но пока локальная развязка через `Waveform` уже снимает основную путаницу.

## Рекомендуемый маршрут чтения

1. Начать с `[[Audio Technology]]` как общей технической рамки.
2. Затем перейти к `[[Sound Synthesis]]` как ветке искусственного звукообразования.
3. После этого открыть `[[Waveform]]` как обзорную развилку между слышимой формой сигнала и управляющей формой сигнала.
4. Затем читать `[[Audio-Rate Waveform]]`, если нужен контекст осцилляторов, спектра и тембра.
5. Читать `[[Control-Rate Waveform]]`, если нужен контекст modulation shapes, LFO и других управляющих сигналов.
6. Затем переходить к `[[Wavetable Synthesis]]`, если нужен частный случай синтеза, где тембр меняется за счет сканирования таблицы волн.

## Соседние overview-ветки

- Родительская рамка: `[[Audio Technology]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом с `Waveform` нужны `Oscillator`, `Envelope` и `Filter`
- [ ] Уточнить границу между `Waveform` как общей формой сигнала и `Wavetable` как организованным набором форм волны
- [ ] Решить, когда `Control-Rate Waveform` пора вынести в отдельную ветку modulation или control signals
- [ ] Проверить границу между synthesis terms и общей signal-processing терминологией
- [ ] Проверить `related`
