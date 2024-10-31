---
slug: "/post5"
title: "Отправка результата прямых операций"
metaTitle: "Отправка результата прямых операций"
sort: "5"
---


После того, как пользователь выберет нужные сертификаты КриптоАРМ выполняет операцию. Полученные файлы отправляется POST-запросом. Используются нотификации (уведомления), для которых не требуется ответ сервера.

## Формат запроса

| Ключ | Значение | Описание |
| --- | --- | --- |
| jsonrpc | «2.0» | Версия JSON-RPC протокола. Всегда «2.0». |
| method | `signAndEncrypt.outDirectResults`|  Используемый метод. Всегда `signAndEncrypt.outDirectResults`. |
| params |  Объект типа [`IDirectResults`](./15-IDirectResults.md) |  Сведения о результатах прямой операции |

Пример:

``` py linenums="1"
Content-Type: application/json
Content-Length: ...
Accept: application/json
{
    "jsonrpc": "2.0",
    "method": "signAndEncrypt.outDirectResults",
    "params": {
        "id": "2c48eb32-a0a8-405c-ade9-eed130605cba",
        "directResults": [
          {
            "id": 2
		"out": "MIIWgQYJKoZIhvcNAQcCoIIWcjCCFm4CA…cN/aHmA="
          }
        ]
    }
}
```
