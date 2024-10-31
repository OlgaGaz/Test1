---
slug: "/post10"
title: "Интерфейс ISystemInformation"
metaTitle: "Интерфейс ISystemInformation"
sort: "10"
---


Объекты данного типа содержат сведения о системе пользователя.

| Свойство | Тип | Описание |
| --- | --- | --- |
| type | string | Тип системы. Возможные значения: 'Linux', 'Darwin' и 'Windows_NT' |
| arch | string | Архитектура операционной системы. Возможные значения: 'arm', 'arm64', 'ia32', 'mips', 'mipsel', 'ppc', 'ppc64', 's390', 's390x', 'x32', и 'x64' |
| platform | string | Имя платформы. Возможные значения: 'aix', 'darwin', 'freebsd', 'linux', 'openbsd', 'sunos', и 'win32' |
| packageType? | string | Необязательный параметр. Тип поддерживаемого пакета (инсталлятора). Возможные значения: ‘msi’, ‘pkg’, ‘rpm’ или ‘deb’ |