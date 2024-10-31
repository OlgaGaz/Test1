---
slug: "/post4"
title: "Получение параметров операции"
metaTitle: "Получение параметров операции"
sort: "4"
---

После получения команды `certrequests ` КриптоАРМ отправляет запрос на получение параметров операции.

## Формат запроса

| Ключ | Значение | Описание |
| --- | --- | --- |
| jsonrpc | «2.0» | Версия JSON-RPC протокола. Всегда «2.0». |
| method | `certrequests.parameters`|  Используемый метод. Всегда `certrequests.parameters`. |
| id |  Уникальный идентификатор |  Используется идентификатор, который указан в ссылке на операцию. Подробнее в разделе [Формат ссылки](../002-description-requests-and-responses.md) |
| diagnostic |  IDiagnosticInformaton |  Диагностическая информация о рабочем месте |

Пример:

``` py linenums="1"
Content-Type: application/json
Content-Length: ...
Accept: application/json
{
    "jsonrpc": "2.0",
    "method": "certrequests.parameters",
    "id": "2c48eb32-a0a8-405c-ade9-eed130605cba",
    "diagnostic": {
    }
}
```

## Формат ответа

| Ключ | Значение | Описание |
| --- | --- | --- |
| jsonrpc | «2.0» | Версия JSON-RPC протокола. Всегда «2.0». |
| result | [`ICertrequestsParameters`](./06-ICertrequestsParameters.md) |  Объект со сведениями о параметрах операции |
| id |  Уникальный идентификатор |  Используется идентификатор, который указан в ссылке на операцию. Подробнее в разделе [Формат ссылки](../002-description-requests-and-responses.md) |

Пример ответа:

``` py linenums="1"
HTTP/1.1 200 OK
Connection: close
Content-Length: ...
Content-Type: application/json
Date: Sat, 08 Jul 2020 12:04:08 GMT
{
    "jsonrpc": "2.0",
    "result": {
        "operation": "GENERATE",
        "props": {
            "templateType": "JSONTemplate",
            "template": {
                "Description": "",
                "FriendlyName": "Пользователь",
                "RDN": [{
                    "Oid": "2.5.4.3",
                    "Name": "CN",
                    "Length": 64,
                    "LocalizedName": "Общее имя",
                    "SettingsValues": [],
                    "DefaultValue": null,
                    "ProhibitAnyValue": false,
                    "ProhibitChange": false,
                    "ProhibitEmpty": true
                }],
                "Extensions": {
                    "KeyUsage": [{
                        "Name": "cRLSign",
                        "LocalizedName": "Автономное подписание списка отзыва (CRL)",
                        "DefaultValue": false,
                        "ProhibitChange": true
                    }],
                    "ExtendedKeyUsage": [{
                        "Name": "1.3.6.1.5.5.7.3.1",
                        "LocalizedName": "Проверка подлинности сервера",
                        "DefaultValue": false,
                        "ProhibitChange": true
                    }]
                },
                "MarkExportable": false
            },
            "id": "2c48eb32-a0a8-405c-ade9-eed130605cba"
        }
    }
}
```