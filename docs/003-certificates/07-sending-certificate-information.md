---
slug: "/post7"
title: "Отправка сведений о сертификате"
metaTitle: "Отправка сведений о сертификате"
sort: "7"
---


После того, как пользователь выберет нужный сертификат КриптАРМ отправляет запрос, содержащий выбранные элементы (base64 без заголовков). Используются нотификации (уведомления), для которых не требуется ответ сервера.

## Формат запроса

| Ключ | Значение | Описание |
| --- | --- | --- |
| jsonrpc | «2.0» | Версия JSON-RPC протокола. Всегда «2.0». |
| method | `certificates.information`| Используемый метод. Всегда `certificates.information`. |
| params | Объект типа [`ICertificateInfo`](./11-ICertificateInfo.md) | Сведения о сертификате |

``` py linenums="1"
Content-Type: application/json
Content-Length: ...
Accept: application/json
{
    "jsonrpc": "2.0",
    "method": "certificates.information",
    "params": {
        "id": "2c48eb32-a0a8-405c-ade9-eed130605cba",
        "hash": "MIIFFDCCBMGgAwIBAgIQTm1HiybyfWV",
        "issuerFriendlyName": "Минкомсвязь России",
        "issuerName": "Минкомсвязь России",
        "subjectFriendlyName ": "Минкомсвязь России",
        "subjectName": "Минкомсвязь России",
        "status": true
    }
}
```