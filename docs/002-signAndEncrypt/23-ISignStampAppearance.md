---
slug: "/post23"
title: "Интерфейс ISignStampAppearance"
metaTitle: "Интерфейс ISignStampAppearance"
sort: "23"
---


Интерфейс `ISignStampAppearance` описывает параметры для штампа PDF.

| Свойство | Тип | Описание |
| --- | --- | --- |
| mockupSettings | [`IMockupSettings`](./24-IMockupSettings.md) | Настройки внешнего вида штампа подписи |
| requisitesSettings | [`IRequisitesSettings`](./25-IRequisitesSettings.md) | Настройки содержимого штампа (реквизиты) |
| pageSelection | string | Определяет, на какой странице или страницах будет отображаться штамп. Возможные значения: «all» – штамп на всех страницах, «last» – штамп на последней странице, «some» – штамп на некоторых страницах. |
| pageNumbers? | string | Необязательный параметр. Страница или диапазон страниц. Пример: «3» или «1-7». |