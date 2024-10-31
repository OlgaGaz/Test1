---
slug: "/post6"
title: "Отправка результата обратных операций"
metaTitle: "Отправка результата обратных операций"
sort: "6"
---


Результаты отправляется POST-запросом. Используются нотификации (уведомления), для которых не требуется ответ сервера.

## Формат запроса

| Ключ | Значение | Описание |
| --- | --- | --- |
| jsonrpc | «2.0» | Версия JSON-RPC протокола. Всегда «2.0». |
| method | `signAndEncrypt.outReverseResults`|  Используемый метод. Всегда `signAndEncrypt.outReverseResults`. |
| params |  Объект типа `IReverseResults`  |  Сведения о результатах обратной операции |

Пример:

``` py linenums="1"
Content-Type: application/json
Content-Length: ...
Accept: application/json
{
    "jsonrpc": "2.0",
    "method": "signAndEncrypt.outReverseResults",
    "params": {
        "id": "2c48eb32-a0a8-405c-ade9-eed130605cba",
        "reverseResults": [
          {
            "out": "MIIWgQYJKoZIhvcNAQcCoIIWcjCCFm4CA…cN/aHmA="
          }
        ]
    }
}
```