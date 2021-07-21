---
description: Contains settings related to managing image catalogs.
solution: Experience Manager
title: catalog-server.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 55e55381-3828-4937-8746-a74e82d6ca38
---
# catalog-server.conf{#catalog-server-conf}

Contains settings related to managing image catalogs.

This file is a JAVA properties file. Care must be taken to follow the appropriate conventions; otherwise the Platform Server may fail to start. Use a double backslash '\\' or a single forward slash '/' instead of a backslash '\' in Windows file paths. The backslash is used as an escape character in this type of file.

Changes to this file take effect shortly after the file is saved.

Only settings listed below may be changed in [!DNL catalog-service.conf]. If a particular setting is absent, it can be added anywhere in the file. Only one instance of each setting may be present.

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
