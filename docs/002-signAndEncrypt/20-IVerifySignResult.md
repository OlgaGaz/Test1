---
slug: "/post20"
title: "Интерфейс IVerifySignResult"
metaTitle: "Интерфейс IVerifySignResult"
sort: "20"
---


Объекты данного типа описывают результаты проверки подписи.

| Свойство | Тип | Описание |
| --- | --- | --- |
| id | string | Идентификатор исходного файла |
| signValid | boolean | Общий статус проверки подписи |
| signers | [`ISignerStatus[]`](./21-ISignerStatus.md) | Информация о подписчиках документа |