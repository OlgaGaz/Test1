---
slug: "/post1"
title: "Общее описание"
metaTitle: "Общее описание"
sort: "1"
---

## Общее описание

КриптоАРМ поддерживает API с двумя возможными точками вызова: 
 - локальное приложение на рабочем месте,
 - web-приложение (сервис). 

При вызове операции через API КриптоАРМ будет запущен и отобразит необходимый раздел с переданными параметрами. Команду можно ввести через адресную строку браузера (вы можете размещать их так же, как ссылки на веб-страницы) или в терминале. Для взаимодействия используется зарегистрированный протокол **cryptoarm://**

В текущей редакции доступны команды:
| Команда | Описание |
| ----------- | ----------- |
| [signAndEncrypt](./01-signAndEncrypt-command-description.md)    | выполнение криптографических операций над документами (подпись, шифрование, проверка подписи, расшифрование)   |
| certificates   |  экспорт или импорт сертификатов, просмотр свойств сертификата   |
| certrequests    | генерация запросов на сертификат   |
| diagnostics     | диагностика рабочего места   |
| startView    | открыть окно или вкладку   |
| mail     | действия с электронными письмами   |

Общий сценарий выполнения команд (для взаимодействия с web-приложениями):
Пользователь заходит на портал (web-приложение).
Выбирает объекты (например список документов) и действие (например подпись).
Портал генерирует и отображает (или сразу переходит) ссылку с протоколом cryptoarm://
Если КриптоАРМ не запущен, то запускается. Затем обращается к порталу за JSON с набором параметров, нужных для выполнения конкретной операции. JSON генерируется на сервере, где располагается web-приложение.
Полученный JSON обрабатывается и в зависимости от команды выполняются нужные дополнительные запросы к web-приложению.
Пользователь подтверждает саму запрошенную операцию (остальной функционал приложения блокируется).
Результаты отправляются на сервер.

Общий сценарий выполнения команд (для взаимодействия с локальным приложением):
Пользователь открывает стороннее приложение, в котором есть поддержка КриптоАРМ API.
Выбирает объекты (например список документов) и действие (например подпись).
Приложение генерирует объект (JSON) и передает на исполнение параметром в КриптоАРМ.
Если КриптоАРМ не запущен, то запускается. Затем обращается к порталу за JSON с набором параметров, нужных для выполнения конкретной операции. JSON генерируется на сервере, где располагается web-приложение.
Полученный JSON обрабатывается.
Пользователь подтверждает саму запрошенную операцию (остальной функционал приложения блокируется).
Результаты сохраняются в локальную папку, переданную в параметрах операции.

Общий формат ссылки для web КриптоАРМ API:
cryptoarm://<command>/<URL>/?id=<id>
Здесь:
cryptoarm:// - зарегистрированный протокол
<command> - выполняемая команда
<URL> - ссылка на получение JSON с параметрами, нужными для выполнения команды
?id=<id> - обязательный параметр. Идентификатор транзакции.

Общий формат команды для локального варианта КриптоАРМ API:
Вариант 1: cryptoarm://<command>/<URI>
Здесь:
cryptoarm:// - зарегистрированный протокол
<command> - выполняемая команда
<URI> - путь к файлу JSON с параметрами, нужными для выполнения команды
Вариант 2: cryptoarm://<command>/<JSON>
Здесь:
cryptoarm:// - зарегистрированный протокол
<command> - выполняемая команда
<JSON> - JSON с параметрами, нужными для выполнения команды