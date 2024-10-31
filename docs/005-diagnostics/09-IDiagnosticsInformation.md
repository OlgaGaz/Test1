---
slug: "/post09"
title: "Интерфейс IDiagnosticsInformation"
metaTitle: "Интерфейс IDiagnosticsInformation"
sort: "09"
---


Объекты данного типа описывают объекты, содержащие сведения о рабочем месте.

| Свойство | Тип | Описание |
| --- | --- | --- |
| id | string | Идентификатор транзакции |
| API_VERSION | string | Версия поддерживаемого КриптоАРМ API |
| SYSTEMINFORMATION | [`ISystemInformation`](./10-ISystemInformation.md) | Сведения о системе |
| CSP_ENABLED | boolean | Установлен или нет КриптоПро CSP |
| CADES_ENABLED | boolean | Доступность CADES |
| VERSIONS | [`IVersions`](./11-IVersions.md) | Версии компонентов |
| PROVIDERS | [`IProviders`](./12-IProviders.md) | Сведения о провайдерах |
| LICENSES | [`ILicenses`](./13-ILicenses.md) | Сведения о лицензиях |
| PERSONALCERTIFICATES | [`ICertificateIdentityInfo[]`](../003-certificates/12-ICertificateIdentityInfo.md ) | Сведения о личных сертификатах (только идентификаторы) |