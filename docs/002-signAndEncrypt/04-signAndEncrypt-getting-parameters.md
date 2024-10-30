---
slug: "/post4"
title: "Получение параметров операции"
metaTitle: "Получение параметров операции"
sort: "4"
---

После получения команды `signAndEncrypt` КриптоАРМ отправляет запрос на `<URL>` для получения параметров операции.

## Формат запроса

| Ключ | Значение | Описание |
| --- | --- | --- |
| jsonrpc | «2.0» | Версия JSON-RPC протокола. Всегда «2.0». |
| method |  [ISignAndEncryptParameters](./08-ISignAndEncryptParameters.md) |  Используемый метод. Всегда `signAndEncrypt.parameters`. |
| id |  Уникальный идентификатор |  Используется идентификатор, который указан в ссылке на операцию. Подробнее в разделе [Формат ссылки](./02-signAndEncrypt-link-format.md) |
| diagnostic |  IDiagnosticInformaton |  Диагностическая информация о рабочем месте |

Пример:

``` py linenums="1"
Content-Type: application/json
Content-Length: ...
Accept: application/json
{
    "jsonrpc": "2.0",
    "method": "signAndEncrypt.parameters",
    "id": "2c48eb32-a0a8-405c-ade9-eed130605cba",
    "diagnostic": {
	}
}
```

## Формат ответа

| Ключ | Значение | Описание |
| --- | --- | --- |
| jsonrpc | «2.0» | Версия JSON-RPC протокола. Всегда «2.0». |
| result |  [ISignAndEncryptParameters](./08-ISignAndEncryptParameters.md) |  Объект со сведениями о параметрах операции подписи |
| id |  Уникальный идентификатор |  Используется идентификатор, который указан в ссылке на операцию. Подробнее в разделе [Формат ссылки](./02-signAndEncrypt-link-format.md) |
| appName? |  string |  Необязательный параметр. Используется только для локального API. Если значение передано, то КриптоАРМ отобразит это название в окне подтверждения операции как название стороннего приложения. |
| apiKey? |  string |  Необязательный параметр. Используется только для локального API. Если значение передано, то КриптоАРМ отобразит это значение в окне подтверждения операции как проверочный код. |

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
        "operation": [
            "SIGN",
            "ARCHIVE",
            "ENCRYPT"
        ],
        "props": {
            "headerText": "Подпись документов cryptoarm.ru",
            "license": "",
            "files": [{
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
            "extra": {
                "token": "9c7101f7-9c47-4481-b4da-a6a497abde08",
                "signType": "1",
                "signStandart": "1"
            },
            "uploader": "http://localhost:8080/upload"
        }
    },
    "id": "2c48eb32-a0a8-405c-ade9-eed130605cba"
}

```