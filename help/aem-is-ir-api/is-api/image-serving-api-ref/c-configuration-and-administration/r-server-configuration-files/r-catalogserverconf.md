---
description: Contains settings related to managing image catalogs.
seo-description: Contains settings related to managing image catalogs.
seo-title: catalog-server.conf
solution: Experience Manager
title: catalog-server.conf
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 797a43d2-18f5-4735-8b19-da231952b1a2
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
