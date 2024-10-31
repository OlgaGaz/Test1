---
slug: "/post15"
title: "Интерфейс IDirectResults"
metaTitle: "Интерфейс IDirectResults"
sort: "15"
---


Объекты данного типа описывают результаты прямой операции.

| Свойство | Тип | Описание |
| --- | --- | --- |
| id | string | Используется идентификатор, который указан в ссылке на операцию ([Формат ссылки](../002-description-requests-and-responses.md)). |
| status | string | Статус выполнения операции. В случае успеха «Completed». |
| directResults | [`IDirectResultOut[]`](./16-IDirectResultOut.md) |  Массив результатов прямых операций |
