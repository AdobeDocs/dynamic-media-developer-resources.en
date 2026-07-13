---
description: Target definition for a click action in the browser.
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 58478e7c-e3a1-4dd5-8ff9-e9752301b93c
TQID: 'https://experienceleague.adobe.com/x27LpaNACQ5k-n09O-9Bhw7aecAjWQ6wNkLt8XewVXs'
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
# [!DNL ImageMapDefinition]{#imagemapdefinition}

Target definition for a click action in the browser.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  name  | `xsd:string`  | The name of the image map definition.  |
|  shapeType  | `xsd:string`  | One of region shape values.  |
|  region  | `xsd:string`  |Image map coordinates. The format is based on the HTML `<area>` tag attributes.  |
|  action  | `xsd:string`  |Other attributes to include in the HTML `<area>` tag, including the `href` URL.  |
|  enabled  | `xsd:boolean`  | True if the image map is enabled.  |

