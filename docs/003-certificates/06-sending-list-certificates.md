---
slug: "/post6"
title: "Отправка списка сертификатов"
metaTitle: "Отправка списка сертификатов"
sort: "6"
---


При экспорте сертификатов результат отправляются на сервер. Если параметры `ICertRequestParameters` содержат поле «multy» со значением «true», то пользователю в КриптоАРМ будет разрешён множественный выбор сертификатов. После того, как пользователь выберет нужные сертификаты и нажмет кнопку «Готово», КриптоАРМ отправляет запрос, содержащий выбранные элементы (base64 без заголовков). Используются нотификации (уведомления), для которых не используется ответ сервера.

## Формат запроса

| Ключ | Значение | Описание |
| --- | --- | --- |
| jsonrpc | «2.0» | Версия JSON-RPC протокола. Всегда «2.0». |
| method | `certificates.base64`| Используемый метод. Всегда `certificates.base64`. |
| params | [`ICertificateBase64Params`](./10-ICertificateBase64Params.md) | Параметры, содержащие объект сертификата |

``` py linenums="1"
Content-Type: application/json
Content-Length: ...
Accept: application/json
{
    "jsonrpc": "2.0",
    "method": "certificates.base64",
    "params": {
        "id": "2c48eb32-a0a8-405c-ade9-eed130605cba",
        "certificates": [{
                "certificateBase64": "MIIFFDCCBMGgAwIBAgIQTm1HiybyfWV...4VVkDWbX/n4=",
                "friendlyName": "Минкомсвязь России"
            },
            {
                "certificateBase64": "MIIFFDCCBMGgAwIBAgIQTm1HiybyfWV...4VVkDWbX/n4=",
                "friendlyName": "Головной удостоверяющий центр"
            }
        ]
    }
}
```