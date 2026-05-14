---
description: Disk space statistics for an asset or folder.
solution: Experience Manager
title: DiskUsage
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a3c4c1cd-0fcc-4e7a-a4aa-884d0ce2f208
TQID: 'https://experienceleague.adobe.com/Md0oAgpJDqSrn1JRZsebpaZKeXIAoLcgkC5KPaHad5s'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# [!DNL DiskUsage]{#diskusage}

Disk space statistics for an asset or folder.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  companyHandle  | `xsd:string`  | Company handle.  |
|  companyName  | `xsd:string`  | Company name.  |
|  imageCount  | `xsd:int`  | Number of stored images.  |
|  diskSpaceUsage  | `xsd:long`  | Total file side in kilobytes.  |
|  lastModified  | `xsd:dateTime`  |Date, time, and time zone the `DiskUsage` type was last modified.  |
