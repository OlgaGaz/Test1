---
slug: "/post7"
title: "Отправка результата проверки подписи"
metaTitle: "Отправка результата проверки подписи"
sort: "7"
---

Результаты проверки подписи отправляется POST запросом. Используются нотификации (уведомления), для которых не требуется ответ сервера.

## Формат запроса

| Ключ | Значение | Описание |
| --- | --- | --- |
| jsonrpc | «2.0» | Версия JSON-RPC протокола. Всегда «2.0». |
| method | `signAndEncrypt.verifySignResults`|  Используемый метод. Всегда `signAndEncrypt.verifySignResults`. |
| params |  Объект типа `IVerifySignResults`  |  Сведения о проверке подписи |

Пример:

``` py linenums="1"
Content-Type: application/json
Content-Length: ...
Accept: application/json
{
    "jsonrpc": "2.0",
    "method": "signAndEncrypt.verifySignResults",
    "params": {
        "id": "2c48eb32-a0a8-405c-ade9-eed130605cba",
        "verifyResults": [
          {
            "id": 2,
            "status": false,
            "signers": [
              {
                "hash": "MIIFFDCCBMGgAwIBAgIQTm1HiybyfWV",
                "issuerFriendlyName": "Минкомсвязь России",
                "issuerName": "Минкомсвязь России",
                "subjectFriendlyName ": "Минкомсвязь России",
                "subjectName": "Минкомсвязь России",
                "status": true
              }
             ]
          }
        ]
    }
}
```