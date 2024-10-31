---
slug: "/post5"
title: " Отправка запроса на сертификат"
metaTitle: " Отправка запроса на сертификат"
sort: "5"
---


После генерации запроса, он будет отправлен на сервер. Используются нотификации (уведомления), для которых не требуется ответ сервера.

## Формат запроса

| Ключ | Значение | Описание |
| --- | --- | --- |
| jsonrpc | «2.0» | Версия JSON-RPC протокола. Всегда «2.0». |
| method | `certrequests.base64`| Используемый метод. Всегда `certrequests.base64`. |
| params |  [`ICertificaterequestBase64Param`](./15-ICertificaterequestBase64Params.md) | Параметры, содержащие объект сертификата |

Пример:

``` py linenums="1"
Content-Type: application/json
Content-Length: ...
Accept: application/json
{
    "jsonrpc": "2.0",
    "method": "certrequests.base64",
    "params": {
        "id": "2c48eb32-a0a8-405c-ade9-eed130605cba",
        "certificaterequestBase64": "MIIFFDCCBMGgAwIBAgIQTm1HiybyfWV...4VVkDWbX/n4=",
        "friendlyName": "ООО Рога и Копыта"
    }
}
```