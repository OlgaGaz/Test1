---
slug: "/post8"
title: "Интерфейс ISignAndEncryptParameters"
metaTitle: "Интерфейс ISignAndEncryptParameters"
sort: "8"
---

Объекты данного типа описывают вид операции и её параметры.

| Свойство | Тип | Описание |
| --- | --- | --- |
| operation | string[] | Тип операции. Доступные значения типов (комбинировать различные типы нельзя): [`ISignAndEncryptOperationDirect`](./09-ISignAndEncryptOperationDirect.md), [`ISignAndEncryptOperationReverse`](./10-ISignAndEncryptOperationReverse.md), [`ISignAndEncryptOperationVerify`](./11-ISignAndEncryptOperationVerify.md) |
| props | [`ISignAndEncryptOperationProps`](./12-ISignAndEncryptOperationProps.md)|  Параметры операции |