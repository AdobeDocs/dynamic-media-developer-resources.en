---
title: Resource root folders (ir.resourceRootPaths)
description: A list of paths, delimited by semi-colons, serve as roots for all data files with relative file paths.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
TQID: https://experienceleague.adobe.com/A8qj55PqIj7-KxO84hmvGRInegVCpRamnWDINQ8EHpw
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
# Resource root folders (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

A list of paths, delimited by semi-colons, serve as roots for all data files with relative file paths.

It can either be absolute paths or paths relative to *[!DNL install_folder]*. When multiple paths are specified, the server tries each root in the given order until the file is found. The default is [!DNL ./resources], for a default root path of [!DNL install_folder/resources].
