---
slug: "/post5"
title: "Интерфейс IStartViewParameters"
metaTitle: "Интерфейс IStartViewParameters"
sort: "5"
---


Объекты данного типа описывают вид операции и её параметры.

| Ключ | Значение | Описание |
| --- | --- | --- |
| uiView | string | Тип окна, которое нужно отобразить пользователю. Доступные значения: “MAIL” – окно почты, “DOCUMENTS” – окно Документы, “SIGN_AND_ENCRYPT” - окно подписи и шифрования, “CERTIFICATES_MY” - окно Сертификаты/Личные сертификаты, “CERTIFICATES_ADDRESS_BOOK” - окно Сертификаты/Другие пользователи, “CERTIFICATES_CA” - окно Сертификаты/Промежуточные, “CERTIFICATES_ROOT” - окно Сертификаты/Корневые, “CONTACTS” - окно Контакты, “KEYS” - окно Сертификаты/Список контейнеров, “ABOUT” и  “DIAGNOSTIC” - окно О программе (Настройки).|
| props | [`IStartViewOperationProps`](../006-startView/06-IStartViewOperationProps.md) | Параметры операции |