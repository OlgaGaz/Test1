---
slug: "/post8"
title: "Интерфейс ICertrequestsOperationGenerateProps"
metaTitle: "Интерфейс ICertrequestsOperationGenerateProps"
sort: "8"
---


Объекты данного типа описывают дополнительные свойства операции.

| Свойство | Тип | Значение | Описание |
| --- | --- | --- | --- |
| headerText? | string | Необязательный параметр. Используется для отображения в заголовке окна. Максимальная длина: 40 символов. | headerText? |
| descriptionText? | string | Необязательный параметр. Используется для отображения в сведениях об операции. Максимальная длина: 120 символов. | descriptionText? |
| templateType | string | JSONTemplate или CertificateTemplate | В качестве шаблона используется JSON типа IJSONTemplate или в качестве шаблона используется сертификат |
| template | [`IJSONTemplate`](./09-IJSONTemplate.md) или [`ICertificateTemplate`](./14-ICertificateTemplate.md) | Шаблон для генерации запроса на сертификат |  |