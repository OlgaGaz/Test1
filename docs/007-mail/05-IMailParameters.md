---
slug: "/post5"
title: "Интерфейс IMailParameters"
metaTitle: "Интерфейс IMailParameters"
sort: "5"
---


Объекты данного типа описывают вид операции и её параметры.

| Свойство | Тип | Описание |
| --- | --- | --- |
| operation | string | Тип операции. Доступные значения: «SEND» – открыть новое сообщение (черновик) с переданными параметрами, «OPEN» – открыть для чтения сообщение eml. |
| props | [`IMailOperationProps`](./06-IMailOperationProps.md) | Параметры операции |