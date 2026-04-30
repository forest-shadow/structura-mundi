# Large Language Models Structure Proposal

## Назначение

Этот файл фиксирует локальную иерархию заметок для ветки `Large Language Models`, в которую естественно помещается рассмотрение таких понятий, как `Transformer Architecture`, `Fine-Tuning`, `Retrieval-Augmented Generation` и `Prompt Engineering`, по правилам `Principia Rerum`.

Ветка размещается внутри уже существующей AI Foundations-ветки и не требует нового `section`:

- `area: computer-science`
- `domain: artificial-intelligence`
- `section: ai-foundations`

`Large Language Models` здесь разумно повышать до `sub-overview`, потому что вокруг темы уже есть несколько самостоятельных дочерних понятий, а `parent` по правилам `Principia Rerum` должен указывать на обзорный узел, а не на обычную `article`.

## Рекомендуемая иерархия

```text
AI Foundations
└── Large Language Models
    ├── Transformer Architecture
    ├── Fine-Tuning
    ├── Prompt Engineering
    └── Retrieval-Augmented Generation
```

## Почему структура именно такая

- `Large Language Models` уже перестает быть одной изолированной статьей и начинает работать как входная рамка для нескольких устойчивых подпонятий.
- `Transformer Architecture` лучше держать рядом с LLM как архитектурное основание, а не смешивать с общими заметками про deep learning, пока корпус именно LLM-ветки важнее общей нейросетевой таксономии.
- `Fine-Tuning`, `Prompt Engineering` и `Retrieval-Augmented Generation` представляют три разных режима влияния на поведение LLM-системы: через параметры модели, через входной контекст и через внешний retrieval-слой.
- Между ними не нужен дополнительный промежуточный `sub-overview`, потому что для стартового корпуса из четырех дочерних узлов это добавило бы лишний уровень вложенности.

## Что не нужно создавать заранее

- отдельный `section` вроде `large-language-models`, пока ветка остается локальным подкластером внутри `ai-foundations`;
- отдельные тематические template-файлы под LLM, потому что по `Principia Rerum` в vault должны оставаться только канонические `Article Template` и `Overview Template`;
- раннее дробление `Prompt Engineering` на техники вроде few-shot, chain-of-thought, system prompting и structured prompting, пока не накопился отдельный корпус.

## Созданные заготовки

- `Large Language Models.md`
- `Transformer Architecture.md`
- `Fine-Tuning.md`
- `Prompt Engineering.md`
- `Retrieval-Augmented Generation.md`

## Следующий шаг

1. Наполнить `Transformer Architecture` базовым механизмом attention, positional encoding и decoder-style transformer stack.
2. Развести границы между `Fine-Tuning` и `Prompt Engineering`, чтобы одно не подменяло другое.
3. Позже решить, нужен ли рядом отдельный узел про `Instruction Tuning`, `Embeddings`, `Context Engineering` или `LLM Evaluation`.
