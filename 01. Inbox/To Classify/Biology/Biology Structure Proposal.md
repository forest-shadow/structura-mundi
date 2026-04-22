# Biology Structure Proposal

## Краткое определение

Этот файл фиксирует рабочую иерархию `Biology` по правилам `Principia Rerum`.

`Biology` остается `area-level root overview`: у него пустые `domain` и `section`. Крупные дисциплинарные ветки под ним оформляются как `domain-root overview`; вложенные смысловые кластеры оформляются как `section-level overview`; конкретные понятия, структуры и процессы оформляются как `article`.

## Рекомендуемая иерархия

```text
Biology
├── Foundations of Biology
│   ├── Life
│   ├── Properties of Life
│   ├── Levels of Biological Organization
│   ├── Cell Theory
│   └── Classification of Life
│       ├── Biological Taxonomy
│       ├── Phylogeny
│       ├── Domains of Life
│       │   ├── Bacteria
│       │   ├── Archaea
│       │   └── Eukaryota
│       ├── Prokaryotes
│       └── Eukaryotes
├── Cell Biology
│   ├── Cell
│   ├── Cell Types
│   │   ├── Prokaryotic Cell
│   │   ├── Eukaryotic Cell
│   │   ├── Animal Cell
│   │   └── Plant Cell
│   ├── Cell Structure
│   │   ├── Plasma Membrane
│   │   ├── Cytoplasm
│   │   ├── Nucleus
│   │   ├── Nucleolus
│   │   ├── Ribosome
│   │   ├── Endoplasmic Reticulum
│   │   │   ├── Rough Endoplasmic Reticulum
│   │   │   └── Smooth Endoplasmic Reticulum
│   │   ├── Golgi Apparatus
│   │   ├── Lysosome
│   │   ├── Peroxisome
│   │   ├── Mitochondrion
│   │   ├── Cytoskeleton
│   │   ├── Centrosome
│   │   └── Vesicle
│   ├── Membrane Transport
│   │   ├── Diffusion
│   │   ├── Osmosis
│   │   ├── Facilitated Diffusion
│   │   ├── Active Transport
│   │   ├── Endocytosis
│   │   └── Exocytosis
│   ├── Cell Communication
│   ├── Cell Cycle
│   ├── Cell Division
│   │   ├── Mitosis
│   │   └── Meiosis
│   └── Cell Death
│       ├── Apoptosis
│       └── Necrosis
├── Biochemistry
│   ├── Biomolecules
│   │   ├── Proteins
│   │   ├── Lipids
│   │   ├── Carbohydrates
│   │   ├── Nucleic Acids
│   │   └── ATP
│   ├── Enzymes
│   ├── Bioenergetics
│   ├── Metabolism
│   │   ├── Catabolism
│   │   ├── Anabolism
│   │   ├── Glycolysis
│   │   ├── Citric Acid Cycle
│   │   ├── Electron Transport Chain
│   │   └── Oxidative Phosphorylation
│   └── Redox Biology
│       ├── Redox Reactions
│       ├── Biological Oxidation
│       ├── Reactive Species
│       │   ├── Reactive Oxygen Species
│       │   ├── Reactive Nitrogen Species
│       │   └── Free Radical Chemistry
│       ├── Redox Homeostasis
│       ├── Redox Buffers
│       │   ├── Glutathione System
│       │   ├── Thioredoxin System
│       │   └── NADPH
│       ├── Redox Signaling
│       ├── Antioxidants
│       │   ├── Enzymatic Antioxidants
│       │   └── Non-Enzymatic Antioxidants
│       ├── Oxidative Stress
│       ├── Oxidative Damage
│       │   ├── Lipid Peroxidation
│       │   ├── Protein Oxidation
│       │   └── DNA Oxidative Damage
│       └── Repair and Response Systems
│           ├── DNA Repair
│           ├── Protein Quality Control
│           ├── Autophagy
│           └── Cellular Stress Response
├── Molecular Biology
│   ├── DNA
│   ├── RNA
│   ├── Gene Expression
│   ├── Replication
│   ├── Transcription
│   └── Translation
├── Genetics
├── Physiology
├── Histology
├── Immunology
├── Microbiology
├── Developmental Biology
├── Evolutionary Biology
└── Ecology
```

## Выбранная классификация

- `Foundations of Biology`: `domain: foundations-of-biology`
- `Cell Biology`: `domain: cell-biology`
- `Biochemistry`: `domain: biochemistry`
- `Molecular Biology`: `domain: molecular-biology`
- `Genetics`: `domain: genetics`
- `Physiology`: `domain: physiology`
- `Histology`: `domain: histology`
- `Immunology`: `domain: immunology`
- `Microbiology`: `domain: microbiology`
- `Developmental Biology`: `domain: developmental-biology`
- `Evolutionary Biology`: `domain: evolutionary-biology`
- `Ecology`: `domain: ecology`

## Именование

- `Taxonomy` в этой ветке развернут как `Biological Taxonomy`, потому что в vault уже есть отдельная заметка `[[Taxonomy]]` в knowledge-organization контексте.
- `Biochemistry` уже существует как canonical domain-root overview в `02. Corpus Mundi`, поэтому новые дочерние seed-заметки ссылаются на `[[Biochemistry]]`, а не создают второй `Biochemistry.md` в Inbox.
- `Antioxidants` сохранен как overview внутри `Redox Biology`, но физически размещен в папке `Antioxidants/Antioxidants.md`, чтобы рядом можно было держать дочерние notes.

## Что стоит раскрыть дальше

- [ ] Решить, какие дочерние ветки нужны внутри `Genetics`
- [ ] Решить, какие дочерние ветки нужны внутри `Physiology`
- [ ] Решить, какие дочерние ветки нужны внутри `Ecology`
- [ ] Проверить, какие seed-articles стоит первыми разворачивать в полноценные article

