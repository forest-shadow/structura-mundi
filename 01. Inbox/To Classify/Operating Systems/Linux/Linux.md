---
aliases:
  - GNU Linux
  - GNU/Linux
note_type: overview
area: computer-science
domain: operating-systems
section: linux
parent: "[[Operating Systems]]"
status: seed
related:
  - "[[Linux Kernel]]"
  - "[[Linux Distribution]]"
  - "[[Linux File System]]"
  - "[[Containerization]]"
tags: []
---

# Linux

## Краткое определение области

`Linux` - это section-level overview внутри `operating-systems`, которое собирает заметки о Linux как о семействе систем, выросших вокруг ядра Linux и практической модели его использования в виде дистрибутивов, user space и инфраструктурных механизмов.

## Что входит в эту тему

- `[[Linux Kernel]]`
- `[[Linux Distribution]]`
- `[[Linux File System]]`

## Как устроена ветка

- `Linux` удерживает широкую практическую рамку, в которой слово «Linux» употребляется в инженерной среде.
- `Linux Kernel` нужен, чтобы развести Linux как ядро и Linux как систему в более широком повседневном смысле.
- `Linux Distribution` нужен, чтобы показать, что Linux почти никогда не существует для пользователя как одно лишь ядро, а обычно поставляется как сборка с инструментами, пакетным менеджментом и соглашениями user space.
- `Linux File System` нужен как Linux-specific article про то, как общая тема `File Systems` проявляется в среде Linux через иерархию каталогов, mount points, virtual file systems и системные соглашения.

## Рекомендуемый маршрут чтения

1. Начать с `[[Linux]]` как общей рамки темы.
2. Затем перейти к `[[Linux Kernel]]`, чтобы зафиксировать строгий технический смысл термина.
3. После этого читать `[[Linux Distribution]]`, чтобы понять, как Linux появляется в реальной эксплуатации и распространении.
4. Затем читать `[[Linux File System]]`, чтобы увидеть Linux-specific сторону общей темы `[[File Systems]]`.
5. Затем уже сопоставлять эту ветку с `[[Containerization]]`, если интересует Linux как основа контейнерной изоляции.

## Соседние overview-ветки

- `[[Operating Systems]]`
- `[[Containerization]]`

## Что стоит раскрыть дальше

- [ ] Уточнить границу между `Linux` и `GNU/Linux`
- [ ] Решить, когда рядом нужны `Linux Namespaces` и `cgroups`
- [ ] Добавить связи с общими заметками про процессы, системные вызовы и файловые системы
- [ ] Проверить, когда рядом с `Linux File System` нужны `procfs`, `sysfs` и `Filesystem Hierarchy Standard`
- [ ] Проверить `related`