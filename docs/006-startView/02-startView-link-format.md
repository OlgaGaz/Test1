---
slug: "/post2"
title: "Формат ссылки"
metaTitle: "Формат ссылки"
sort: "2"
---


Для выполнения команды `startView` должна быть сформирована ссылка вида:

```
cryptoarm://startView/<URL>/?id=<id>
```

- `cryptoarm://` - зарегистрированный протокол

- `startView` - выполняемая команда

- `<URL>` - ссылка на получение JSON с параметрами, нужными для выполнения команды

- `id` - уникальный идентификатор транзакции

Пример:

```
cryptoarm://startView/https://example.com/json?id=2c48eb32-a0a8-405c-ade9-eed130605cba
```
