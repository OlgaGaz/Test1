---
slug: "/post10"
title: "Интерфейс IRDN"
metaTitle: "Интерфейс IRDN"
sort: "10"
---


| Свойство | Тип | Описание |
| --- | --- | --- |
| Oid | string | Описание шаблона |
| Name | string | Наименование OID |
| Length | number | Максимальная длина поля |
| LocalizedName | string | Локализованное наименование OID |
| SettingsValues | string[] | Список возможных значений |
| DefaultValue | string | Значение по умолчанию |
| ProhibitAnyValue | boolean | Флаг указывающий, что пользователю доступны только значения из массива `SettingsValues` |
| ProhibitChange | boolean | Флаг указывающий, что поле не может быть изменено |
| ProhibitEmpty | boolean | Флаг указывающий, что поле должно быть непустым |