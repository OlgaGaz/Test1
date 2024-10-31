---
slug: "/post5"
title: "Отправка сертификата"
metaTitle: "Отправка сертификата"
sort: "5"
---

При экспорте сертификатов результат отправляются на сервер. После того, как пользователь выберет нужный сертификат КриптоАРМ отправляет запрос, содержащий выбранные элементы (base64 без заголовков). Используются нотификации (уведомления), для которых не требуется ответ сервера.

## Формат запроса

| Ключ | Значение | Описание |
| --- | --- | --- |
| jsonrpc | «2.0» | Версия JSON-RPC протокола. Всегда «2.0». |
| method | `certificates.base64`| Используемый метод. Всегда `certificates.base64`. |
| params |  [`ICertificateBase64Params`](./10-ICertificateBase64Params.md) | Параметры, содержащие объект сертификата |

Пример:

``` py linenums="1"
Content-Type: application/json
Content-Length: ...
Accept: application/json
{
    "jsonrpc": "2.0",
    "method": "certificates.base64",
    "params": {
        "id": "2c48eb32-a0a8-405c-ade9-eed130605cba",
        "certificateBase64": "MIIFFDCCBMGgAwIBAgIQTm1HiybyfWV...4VVkDWbX/n4=",
        "friendlyName": "Минкомсвязь России"
    }
}
```