---
slug: "/post22"
title: "Интерфейс ILocalResultParams"
metaTitle: "Интерфейс ILocalResultParams"
sort: "22"
---


Объекты данного типа используется только в параметрах локального API. 

Содержат пути для сохранения результатов операций.

| Свойство | Тип | Описание |
| --- | --- | --- |
| savePath? | string | Необязательный параметр. Путь для сохранения результатов операции. |
| saveResultsSeparately? | boolean | Необязательный параметр. Определяет, сохранять ли результаты по каждому файлу в отдельный файл или сохранять в один JSON, один файл. |