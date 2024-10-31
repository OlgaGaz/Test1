---
slug: "/post5"
title: "Отправка сведений о рабочем месте"
metaTitle: "Отправка сведений о рабочем месте"
sort: "5"
---

Полученные сведения отправляется POST запросом. Используются нотификации (уведомления), для которых не требуется ответ сервера.

## Формат запроса

| Ключ | Значение | Описание |
| --- | --- | --- |
| jsonrpc | «2.0» | Версия JSON-RPC протокола. Всегда «2.0». |
| method | `diagnostics.information`| Используемый метод. Всегда `diagnostics.information`. |
| params |  [`IDiagnosticsInformation`](./09-IDiagnosticsInformation.md) | Сведения о рабочем месте |

Пример:

``` py linenums="1"
Content-Type: application/json
Content-Length: ...
Accept: application/json
{
  "jsonrpc": "2.0",
  "method": "diagnostics.information",
  "params": {
    "id": "2c48eb32-a0a8-405c-ade9-eed130605cba",
    "CSP_ENABLED": true,
    "LICENSES": {
      "csp": {
        "status": true,
      },
      "cryptoarm": {
        "status": true,
        "type": "temporary",
        "expiration": "1591689487056",
      }
    },
    "VERSIONS": {
      "csp": "5.0.11753",
      "cryptoarm": "2.5.2",
    }
  }
}
```