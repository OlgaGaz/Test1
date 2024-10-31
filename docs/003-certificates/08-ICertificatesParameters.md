---
slug: "/post8"
title: "Интерфейс ICertificatesParameters"
metaTitle: "Интерфейс ICertificatesParameters"
sort: "8"
---


Объекты данного типа описывают параметры команды запроса на получение сертификат.

| Свойство | Тип | Описание |
| --- | --- | --- |
| operation | string | Тип операции импорт, экспорт, информация. Доступные значения: “import”, “export”, “information” |
| props | [`ICertificatesOperationProps`](./09-ICertificatesOperationProps.md) | Параметры операции |
