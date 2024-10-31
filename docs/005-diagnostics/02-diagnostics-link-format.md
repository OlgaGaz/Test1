---
slug: "/post2"
title: "Формат ссылки"
metaTitle: "Формат ссылки"
sort: "2"
---


Для выполнения команды `diagnostics` должна быть сформирована ссылка вида:


```
cryptoarm://diagnostics/<URL>/?id=<id>
```

- `cryptoarm://` - зарегистрированный протокол

- `diagnostics` - выполняемая команда

- `<URL>` - ссылка, на которую КриптоАРМ будет слать запросы

- `id` - уникальный идентификатор транзакции


Пример:

```
cryptoarm://diagnostics/https://example.com/json?id=2c48eb32-a0a8-405c-ade9-eed130605cba
```