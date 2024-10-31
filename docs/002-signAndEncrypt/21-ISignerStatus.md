---
slug: "/post21"
title: "Интерфейс ISignerStatus"
metaTitle: "Интерфейс ISignerStatus"
sort: "21"
---


Объекты данного типа описывают сведения о подписчиках.

| Свойство | Тип | Описание |
| --- | --- | --- |
| signerCertificate | [`ICertificateInfo`](../003-certificates/11-ICertificateInfo.md) | Сведения о сертификате подписчика |
| isValid | boolean | Статус подписи |
| signingTime | string | Время подписи |