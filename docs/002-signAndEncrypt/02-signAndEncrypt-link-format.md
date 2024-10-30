---
slug: "/post2"
title: "Формат ссылки"
metaTitle: "Формат ссылки"
sort: "2"
---


Для выполнения команды `signAndEncrypt` должна быть сформирована ссылка вида:

```
cryptoarm://<command>/<URL>/?id=<id>
```

- `cryptoarm://` - зарегистрированный протокол

- `<command>` - выполняемая команда

- `<URL>` - ссылка на получение JSON с параметрами, нужными для выполнения команды

- `?id=<id>` - обязательный параметр. Идентификатор транзакции.

Пример:

```
cryptoarm://signAndEncrypt/https://example.com/json?id=2c48eb32-a0a8-405c-ade9-eed130605cba
```
