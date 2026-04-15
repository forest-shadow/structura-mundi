
## Краткое определение

Этот файл фиксирует минимальную иерархию area-level корневой ветки `Anthropology` по правилам `Principia Rerum`.

## Выбранная оптика

- `area: anthropology`
- `domain:` пусто для `area-level root overview`
- `section:` пусто для `area-level root overview`

Почему так:

- `Anthropology` находится выше конкретных доменных веток и не должна подменяться одним частным `domain`;
- обновленная модель `Principia Rerum` явно разрешает для area-level root пустые `domain` и `section`;
- это позволяет оставить корневую заметку действительно обзорной и не вводить искусственные служебные значения.

## Каноническое имя

- корневая обзорная заметка: `Anthropology`
- `Антропология` лучше хранить в `aliases`

## Рекомендуемая иерархия

```text
Anthropology
└── Ethnobiology
    └── Ethnomycology
```

## Почему структура именно такая

- `Anthropology` нужна как root `overview`, потому что это не локальная тема, а вся верхнеуровневая область знания внутри текущей части vault.
- `Ethnobiology` уже оформлена как первый устойчивый domain-root внутри `anthropology`, поэтому именно она должна висеть прямо под корневой заметкой, а не смешиваться с более частными статьями на одном уровне.
- `Ethnomycology` логично оставлять внутри `Ethnobiology`, потому что сейчас это не самостоятельный соседний домен антропологии, а более узкий тематический кластер внутри ethnobiological perspective.

## Что не стоит создавать заранее

- дополнительные domain-root ветки только ради симметрии, если под них пока нет устойчивого корпуса заметок;
- лишние промежуточные overview-слои между `Anthropology` и `Ethnobiology`;
- специальные тематические template-файлы под anthropology: по `Principia Rerum` здесь достаточно канонических `Overview Template` и `Article Template`.

## Что уже создано в Inbox

- `[[Anthropology]]`
- `[[Ethnobiology]]`
- `[[Ethnomycology]]`

## Что стоит раскрыть дальше

- [ ] Проверить, когда внутри `anthropology` появятся другие устойчивые domain-root ветки рядом с `Ethnobiology`
- [ ] Проверить, остается ли `Anthropology` area-level root без `domain` и `section`
- [ ] Проверить `related`
