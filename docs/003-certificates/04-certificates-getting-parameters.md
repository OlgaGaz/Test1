---
slug: "/post4"
title: "Получение параметров операции"
metaTitle: "Получение параметров операции"
sort: "4"
---

После получения команды `certificates` КриптоАРМ отправляет запрос на получение параметров операции.

## Формат запроса

| Ключ | Значение | Описание |
| --- | --- | --- |
| jsonrpc | «2.0» | Версия JSON-RPC протокола. Всегда «2.0». |
| method | `certificates.parameters`|  Используемый метод. Всегда `certificates.parameters`. |
| id |  Уникальный идентификатор |  Используется идентификатор, который указан в ссылке на операцию. Подробнее в разделе [Формат ссылки](../002-description-requests-and-responses.md) |
| diagnostic |  IDiagnosticInformaton |  Диагностическая информация о рабочем месте |

Пример:

``` py linenums="1"
Content-Type: application/json
Content-Length: ...
Accept: application/json
{
    "jsonrpc": "2.0",
    "method": "certificates.parameters",
    "id": "2c48eb32-a0a8-405c-ade9-eed130605cba",
    "diagnostic": {
     }
}
```

## Формат ответа

| Ключ | Значение | Описание |
| --- | --- | --- |
| jsonrpc | «2.0» | Версия JSON-RPC протокола. Всегда «2.0». |
| result | [`ICertificatesParameters`](./08-ICertificatesParameters.md) |  Объект со сведениями о параметрах операции |
| id |  Уникальный идентификатор |  Используется идентификатор, который указан в ссылке на операцию. Подробнее в разделе [Формат ссылки](../002-description-requests-and-responses.md) |

Пример ответа для экспорта сертификата:

``` py linenums="1"
HTTP/1.1 200 OK
Connection: close
Content-Length: ...
Content-Type: application/json
Date: Sat, 08 Jul 2020 12:04:08 GMT
{
    "jsonrpc": "2.0",
    "result": {
        "operation": "export",
        "props": {
            "store": ["MY"],
            "multy": false
        }
    },
    "id": "2c48eb32-a0a8-405c-ade9-eed130605cba"
}
```

Пример ответа для экспорта сертификата:

``` py linenums="1"
HTTP/1.1 200 OK
Connection: close
Content-Length: ...
Content-Type: application/json
Date: Sat, 08 Jul 2020 12:04:08 GMT
{
    "jsonrpc": "2.0",
    "result": {
        "operation": "information",
        "props": {
            "certificateBase64": "MIIFFDCCBMGgAwIBAgIQT...4VVkDWbX/n4="
        }
    },
    "id": "2c48eb32-a0a8-405c-ade9-eed130605cba"
}
```