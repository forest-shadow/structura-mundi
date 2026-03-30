# VPN Structure Proposal

## Краткое определение

Предлагаемое устройство ветки `VPN` внутри `Network Security`.

## Рекомендуемая иерархия

```text
Network Security
└── VPN
    ├── Remote Access VPN
    ├── Site-to-Site VPN
    ├── VPN Tunneling
    └── VPN Protocol Families
```

## Почему структура именно такая

- `VPN` уже лучше оформлять как `sub-overview`, потому что тема естественно распадается не на один аспект, а минимум на сценарии развертывания, механику туннелирования и протокольные семейства.
- `Remote Access VPN` и `Site-to-Site VPN` описывают разные deployment patterns и не должны сливаться в одну общую заметку.
- `VPN Tunneling` нужен как механизм-центричная статья, чтобы не смешивать способ построения канала с business or operational scenario.
- `VPN Protocol Families` удерживает технологическую карту и позволяет позже аккуратно выводить `IPsec`, `OpenVPN`, `WireGuard` и другие notes.

## Что не стоит делать прямо сейчас

- Не стоит заранее создавать полный каталог vendor-specific и protocol-specific notes.
- Не стоит смешивать `VPN` с любой защищенной удаленной связностью без уточнения границ темы.
- Не стоит превращать `VPN` в одну длинную статью, где перемешаны tunnel mechanics, access patterns и protocol families.

## Что стоит раскрыть дальше

- [ ] Решить, когда нужны `IPsec VPN`, `SSL VPN` и `WireGuard`
- [ ] Проверить, нужен ли отдельный article про split tunneling
- [ ] Проверить `related`
