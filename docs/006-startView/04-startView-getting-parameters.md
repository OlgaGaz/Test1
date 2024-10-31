---
slug: "/post4"
title: "Получение параметров операции"
metaTitle: "Получение параметров операции"
sort: "4"
---

После получения команды `startView` КриптоАРМ отправляет запрос на получение параметров операции.

## Формат запроса

| Ключ | Значение | Описание |
| --- | --- | --- |
| jsonrpc | «2.0» | Версия JSON-RPC протокола. Всегда «2.0». |
| method | `startView.parameters`|  Используемый метод. Всегда `startView.parameters`. |
| id |  Уникальный идентификатор | Используется идентификатор, который указан в ссылке на операцию. Подробнее в разделе [Формат ссылки](../002-description-requests-and-responses.md) |
| diagnostic |  [`IDiagnosticInformaton`](../005-diagnostics/09-IDiagnosticsInformation.md) |  Диагностическая информация о рабочем месте |

Пример:

``` py linenums="1"
Content-Type: application/json
Content-Length: ...
Accept: application/json
{
    "jsonrpc": "2.0",
    "method": "startView.parameters",
    "id": "2c48eb32-a0a8-405c-ade9-eed130605cba",
    "diagnostic": {
    }
}

```

## Формат ответа

| Ключ | Значение | Описание |
| --- | --- | --- |
| jsonrpc | «2.0» | Версия JSON-RPC протокола. Всегда «2.0». |
| result |  [`IStartViewParameters`](../006-startView/05-IStartViewParameters.md) |  Объект со сведениями о параметрах операции |
| id |  Уникальный идентификатор |  Используется идентификатор, который указан в ссылке на операцию. Подробнее в разделе [Формат ссылки](../002-description-requests-and-responses.md) |

Пример:

``` py linenums="1"
HTTP/1.1 200 OK
Connection: close
Content-Length: ...
Content-Type: application/json
Date: Sat, 08 Jul 2020 12:04:08 GMT
{
    "jsonrpc": "2.0",
    "result": {
        " uiView": “CERTIFICATES_MY”,
        "props": {
            "headerText": "ИС cryptoarm.ru",
            "descriptionText": "Запрос на открытие окна"
        }
    },
    "id": "2c48eb32-a0a8-405c-ade9-eed130605cba"
}
```