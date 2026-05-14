---
description: Sends an email to a designated recipient in response to a cdnCacheInvalidation operation.
solution: Experience Manager
title: EmailConfirmation
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b4698637-a897-47fa-92d4-4ab400e56962
TQID: 'https://experienceleague.adobe.com/h9ZZRR0zR347mzSifomCmtNW5GorTC6fgGjeSRf52KU'
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
# [!DNL EmailConfirmation]{#emailconfirmation}

Sends an email to a designated recipient in response to a cdnCacheInvalidation operation.

 Syntax 

## Parameters {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

|  Name  | Type  | Description  |
|---|---|---|
|  ccOriginator  | `xsd:boolean`  | If true, includes the user's web service user account, which is a list of emails designated to receive an email confirmation from the Dynamic Media CDN.  |
|  ccOthersArray  | `types:EmailArray`  | An array of email addresses (5 maximum) designated to receive the confirmation notification from the Dynamic Media CDN.  |
