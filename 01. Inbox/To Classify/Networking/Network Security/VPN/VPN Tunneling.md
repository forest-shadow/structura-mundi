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
  - "[[Remote Access VPN]]"
  - "[[Site-to-Site VPN]]"
  - "[[VPN Protocol Families]]"
tags: []
---

# VPN Tunneling

## Краткое определение

`VPN Tunneling` — это статья о механике построения логического канала, в котором один сетевой поток инкапсулируется, защищается и переносится поверх другой транспортной среды.

## Основная идея или механизм

Суть туннелирования в VPN в том, что исходный трафик не передается в исходном виде по всей внешней среде, а упаковывается в защищенную или логически изолированную оболочку, которая и образует tunnel между конечными точками.

## Границы темы

- Входит: encapsulation, logical tunnel, отношение между внутренним и внешним transport path.
- Не входит: конкретные deployment scenarios вроде `Remote Access VPN` и `Site-to-Site VPN`.

## Связи с другими заметками

Родительская тема:

`[[VPN]]`

Связанные заметки:

- `[[Remote Access VPN]]`
- `[[Site-to-Site VPN]]`
- `[[VPN Protocol Families]]`

## Примеры, случаи или следствия

- Инкапсуляция приватного IP-трафика поверх публичной IP-сети.
- Логическое разделение внутреннего адресного пространства и внешнего транспортного пути.

## Что стоит раскрыть дальше

- [ ] Уточнить различие между tunneling, encryption и simple forwarding
- [ ] Добавить связи
- [ ] Проверить `aliases`
- [ ] Проверить `tags`
