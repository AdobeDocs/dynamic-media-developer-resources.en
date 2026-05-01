---
description: Static content source data files are accessed only by the [!DNL Platform Server].
solution: Experience Manager
title: Static content source data
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
TQID: https://experienceleague.adobe.com/KTZvEz07Qa1CLYo6WpK1Lyjd9-dQrIAVFtafPhqH8ao
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
# Static content source data{#static-content-source-data}

Static content source data files are accessed only by the [!DNL Platform Server].

 The path for static content data files is resolved as follows:

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

The server combines path segments right to left until an absolute file path is established.

All ` *[!DNL rootPath]*` segments can be empty, relative, or absolute path segments.

` *[!DNL catalogPath]*` is either an absolute or relative file path/name. *[!DNL requestPath]* must be a relative file path/name.

Multiple `PS::staticContent.rootPaths` values can be defined in [!DNL PlatformServer.conf]. This allows source data files to be distributed across multiple file systems. The [!DNL Platform Server] tries alternate paths in the order specified until the data file is found.
