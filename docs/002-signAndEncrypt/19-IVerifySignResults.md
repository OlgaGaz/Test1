---
slug: "/post19"
title: "Интерфейс IVerifySignResults"
metaTitle: "Интерфейс IVerifySignResults"
sort: "19"
---


Объекты данного типа описывают результаты проверки подписи.

| Свойство | Тип | Описание |
| --- | --- | --- |
| id | string | Используется идентификатор, который указан в ссылке на операцию ([Формат ссылки](../002-description-requests-and-responses.md)). |
| status | string | Статус выполнения операции. В случае успеха « Completed». |
| verifySignResults | [`IVerifySignResult[]`](./20-IVerifySignResult.md) | Массив результатов проверки |