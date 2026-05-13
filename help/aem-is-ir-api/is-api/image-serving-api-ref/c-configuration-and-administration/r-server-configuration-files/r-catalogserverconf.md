---
description: Contains settings related to managing image catalogs.
solution: Experience Manager
title: catalog-server.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 55e55381-3828-4937-8746-a74e82d6ca38
TQID: 'https://experienceleague.adobe.com/GdtVY3WMO9F6C5vzkOHdVoMW-f6-L1cJGUt1KUCvLJ8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# catalog-server.conf{#catalog-server-conf}

Contains settings related to managing image catalogs.

This file is a JAVA properties file. Care must be taken to follow the appropriate conventions; otherwise the [!DNL Platform Server] may fail to start. Use a double backslash '\\' or a single forward slash '/' instead of a backslash '\' in Windows file paths. The backslash is used as an escape character in this type of file.

Changes to this file take effect shortly after the file is saved.

Only settings listed below may be changed in [!DNL catalog-service.conf]. If a particular setting is absent, it can be added anywhere in the file. Only one instance of each setting may be present.

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
