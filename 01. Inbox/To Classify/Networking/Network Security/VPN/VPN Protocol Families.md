---
aliases: []
note_type: article
area: computer-science
domain: networking
section: network-security
parent: "[[VPN]]"
status: draft
related:
  - "[[VPN]]"
  - "[[VPN Tunneling]]"
  - "[[Remote Access VPN]]"
  - "[[Site-to-Site VPN]]"
  - "[[Network Protocols]]"
tags: []
---

# VPN Protocol Families

## Краткое определение

`VPN Protocol Families` — это статья о главных технологических семействах, через которые обычно реализуются VPN: IPsec-based, TLS or SSL-based, WireGuard-like и другие близкие подходы.

## Основная идея или механизм

Эта заметка нужна как карта протокольных семейств VPN, чтобы отделить deployment patterns и tunnel mechanics от выбора конкретной технологической реализации.

## Границы темы

- Входит: семейства реализаций VPN и их общая роль.
- Не входит: подробный разбор каждой конкретной технологии в отдельности, пока для этого нет устойчивого корпуса notes.

## Связи с другими заметками

Родительская тема:

`[[VPN]]`

Связанные заметки:

- `[[VPN Tunneling]]`
- `[[Remote Access VPN]]`
- `[[Site-to-Site VPN]]`
- `[[Network Protocols]]`

## Примеры, случаи или следствия

- Сопоставление IPsec-подходов и TLS-based решений для разных deployment scenarios.
- Выбор семейства реализации меняет требования к клиентам, gateway-узлам и operational complexity.

## Что стоит раскрыть дальше

- [ ] Уточнить минимальный набор protocol families внутри заметки
- [ ] Добавить связи
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
