---
slug: "/post6"
title: "Интерфейс IMailOperationProps"
metaTitle: "Интерфейс IMailOperationProps"
sort: "6"
---


Объекты данного типа описывают вид операции и её параметры.

| Свойство | Тип | Описание |
| --- | --- | --- |
| eml? | [`IFile`](../002-signAndEncrypt/13-IFile.md) | Необязательный параметр. Параметры для получения eml файла. |
| mailProps? | [`IMailProps`](./07-IMailProps.md) | Необязательный параметр. Свойства для нового сообщения. |
| extra? | Объект типа [`IExtra`](../002-signAndEncrypt/14-IExtra.md) | Необязательный параметр. Настройки операции. Для команды `mail` это свойство может содержать token, для скачивания eml с сервера. |