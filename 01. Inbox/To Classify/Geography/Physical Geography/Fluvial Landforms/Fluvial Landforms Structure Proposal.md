# Fluvial Landforms Structure Proposal

## Краткое определение

Этот файл фиксирует минимальную иерархию заметок для ветки `Fluvial Landforms`, в которую естественно помещается рассмотрение такого понятия как `Floodplain` в контексте характера местности у реки, по правилам `Principia Rerum`.

## Выбранная оптика

- `area: geography`
- `domain: physical-geography`
- `section: fluvial-landforms`

Почему так:

- `Floodplain` описывает не культурный или исторический феномен, а форму местности и часть речной долины, связанную с режимом разлива и аккумуляцией наносов;
- существующие `area` вроде `biology`, `anthropology` или `history` здесь не подходят как главная оптика;
- внутри новой области `geography` это понятие естественнее всего читать через `physical-geography`, потому что речь идет о морфологии поверхности, водных процессах и характере рельефа;
- `section: fluvial-landforms` достаточно узок, чтобы собирать рядом будущие заметки о `Levee`, `River Terrace`, `Meander Belt`, `Alluvial Plain` и других формах рельефа, связанных с рекой.

## Канонические имена

- area-level root: `Geography`
- domain-root overview: `Physical Geography`
- section-level overview: `Fluvial Landforms`
- article: `Floodplain`

`Пойма` лучше хранить в `aliases`, а не делать отдельным русскоязычным дублем.

## Рекомендуемая иерархия

```text
Geography
└── Physical Geography
    └── Fluvial Landforms
        └── Floodplain
```

## Почему структура именно такая

- `Geography` нужна как новый area-level root, потому что тема неестественно встраивается в уже существующие области знания.
- `Physical Geography` уместна как domain-root overview, потому что `Floodplain` — это не вся география, а природоведческая ветка о формах поверхности и процессах их формирования.
- `Fluvial Landforms` лучше сделать section-level overview, потому что `Floodplain` — это не изолированный термин, а один из элементов более широкого кластера речного рельефа.
- `Floodplain` должен быть обычной `article`, а не overview, потому что сейчас речь идет об одном конкретном понятии.

## Что не стоит делать прямо сейчас

- не стоит помещать `Floodplain` напрямую под `Geography`, потому что тогда теряется дисциплинарная рамка;
- не стоит относить `Floodplain` к `biology`, если заметка описывает именно форму местности, а не экосистему поймы;
- не стоит создавать отдельные тематические template-файлы под речной рельеф или географию: по `Principia Rerum` здесь достаточно канонических `Overview Template` и `Article Template`, развернутых в конкретные заметки ветки.

## Предлагаемое физическое размещение в Inbox

```text
01. Inbox/
└── To Classify/
    └── Geography/
        └── Physical Geography/
            └── Fluvial Landforms/
                ├── Fluvial Landforms Structure Proposal.md
                ├── Fluvial Landforms.md
                └── Floodplain.md
```

## Что уже создано в этой ветке

- `[[Geography]]`
- `[[Physical Geography]]`
- `[[Fluvial Landforms]]`
- `[[Floodplain]]`

## Что стоит раскрыть дальше

- [ ] Решить, когда рядом с `Floodplain` нужны статьи про `Levee`, `River Terrace` и `Alluvial Plain`
- [ ] Подтвердить `section: fluvial-landforms`
- [ ] Проверить `related`
