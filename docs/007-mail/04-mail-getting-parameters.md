---
slug: "/post4"
title: "Получение параметров операции"
metaTitle: "Получение параметров операции"
sort: "4"
---

После получения команды `mail` КриптоАРМ отправляет запрос на получение параметров операции.

## Формат запроса

| Ключ | Значение | Описание |
| --- | --- | --- |
| jsonrpc | «2.0» | Версия JSON-RPC протокола. Всегда «2.0». |
| method | `mail.parameters`|  Используемый метод. Всегда `mail.parameters`. |
| id |  Уникальный идентификатор |  Используется идентификатор, который указан в ссылке на операцию. Подробнее в разделе [Формат ссылки](../002-description-requests-and-responses.md) |
| diagnostic | [`IDiagnosticInformaton`](../005-diagnostics/09-IDiagnosticsInformation.md) |  Диагностическая информация о рабочем месте |

Пример:

``` py linenums="1"
Content-Type: application/json
Content-Length: ...
Accept: application/json
{
    "jsonrpc": "2.0",
    "method": "mail.parameters",
    "id": "2c48eb32-a0a8-405c-ade9-eed130605cba",
    "diagnostic": {
    }
}

```

## Формат ответа

| Ключ | Значение | Описание |
| --- | --- | --- |
| jsonrpc | «2.0» | Версия JSON-RPC протокола. Всегда «2.0». |
| result | [`IMailParameters`](./05-IMailParameters.md) |  Объект со сведениями о параметрах операции |
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
        "operation": "SEND",
        "props": {
		"mailProps": {
		   "to": ["test@example.com"],
		   "cc": ["test1@example.com", "test2@example.com"],
		   "bcc": ["test3@example.com"],
		   "subject": "Message subject",
		   "content": "text message content",
		   "htmlContent": "<div>HTML message content</div>",
		   "attachments": [{
                    "name": "file1.txt",
                    "url": "http://localhost:8080/public/files/file1.txt",
                    "id": 1,
                    "urlDetached": ""
                },
                {
                    "name": "file2.txt",
                    "url": "http://localhost:8080/public/files/file2.txt",
                    "id": 2,
                    "urlDetached": ""
                },
                {
                    "name": "file4.pdf",
                    "url": "http://localhost:8080/public/files/file4.pdf",
                    "id": 4,
                    "urlDetached": ""
                }
		   ],
		   "sign": false,
		   "encrypt": false,
		   "deliveryReport": false,
		   "readReport": false
		   }
	  }
    },
    "id": "2c48eb32-a0a8-405c-ade9-eed130605cba"
}
```