---
slug: "/post24"
title: "Интерфейс IMockupSettings"
metaTitle: "Интерфейс IMockupSettings"
sort: "24"
---


Интерфейс `IMockupSettings` описывает параметры внешнего вида штампа.

| Свойство | Тип | Описание |
| --- | --- | --- |
| position | string | Положение штампа внутри области. Возможные значения: «fitArea» – вписать, «actualSize» – реальный размер, «fitMockup» – подогнать область под макет. |
| addBackground | boolean | Определяет, будет ли добавлен фон на область |
| addBorders | boolean | Определяет, будет ли добавлена граница на область |
| logotype? | boolean | Необязательный параметр. Использовать или нет логотип для штампа. |