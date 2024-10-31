---
slug: "/post11"
title: "Интерфейс ICertificateInfo"
metaTitle: "Интерфейс ICertificateInfo"
sort: "11"
---


Объекты данного типа описывают объекты, содержащие свойства сертификата.

| Свойство | Тип | Описание |
| --- | --- | --- |
| hash | string | SHA1 отпечаток |
| issuerFriendlyName | string | Дружественное имя издателя (CN) |
| issuerName | string | Имя издателя |
| notAfter | string | Дата окончания действия сертификата |
| notBefore | string | Дата начала действия сертификата |
| rootCAMinComSvyaz | boolean | Флаг, обозначающий является ли владельцем корневого сертификата цепочки “Минкомсвязь России” |
| subjectFriendlyName | string | Дружественное имя субъекта (CN) |
| subjectName | string | Имя субъекта |
| status | boolean | Статус сертификата. Проверяется вся цепочка. |
| serial | string | Серийный номер сертификата |
| x509? | string | Необязательный параметр. Сертификат в формате X.509 закодированный в Base64. |