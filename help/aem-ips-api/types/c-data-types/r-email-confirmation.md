---
description: Sends an email to a designated recipient in response to a cdnCacheInvalidation operation.
solution: Experience Manager
title: EmailConfirmation
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b4698637-a897-47fa-92d4-4ab400e56962
---
# [!DNL EmailConfirmation]{#emailconfirmation}

Sends an email to a designated recipient in response to a cdnCacheInvalidation operation.

 Syntax 

## Parameters {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

|  Name  | Type  | Description  |
|---|---|---|
|  ccOriginator  | `xsd:boolean`  | If true, includes the user's web service user account, which is a list of emails designated to receive an email confirmation from the Dynamic Media CDN.  |
|  ccOthersArray  | `types:EmailArray`  | An array of email addresses (5 maximum) designated to receive the confirmation notification from the Dynamic Media CDN.  |
