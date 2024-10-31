---
slug: "/post9"
title: "Интерфейс ICertificatesParameters"
metaTitle: "Интерфейс ICertificatesParameters"
sort: "9"
---


Объекты данного типа описывают поля для генерации запроса на сертификат.

| Свойство | Тип | Описание |
| --- | --- | --- |
| Description | string | Описание шаблона |
| FriendlyName | string | Дружественное имя шаблона |
| RDN | [`IRDN[]`](./10-IRDN.md) | Набор полей DN |
| Extensions | [`IRequestExtension`](./11-IRequestExtension.md) | Расширения |
| MarkExportable | boolean | Определяет экспортируемость ключей |