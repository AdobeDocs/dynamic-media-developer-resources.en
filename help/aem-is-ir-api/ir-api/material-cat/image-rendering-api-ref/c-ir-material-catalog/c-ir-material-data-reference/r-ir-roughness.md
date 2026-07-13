---
description: Surface roughness. Specifies the relative glossiness of the material surface. Used in conjunction with catalog Type and catalog Gloss to control 3D reflection render effects.
solution: Experience Manager
title: Roughness
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 61d956ec-62dd-4879-877e-2ac422396e2e
TQID: 'https://experienceleague.adobe.com/YvUmUkOLzzbM7Zs-7T35rwYRNrUeh6-QXW339AA3R8Q'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# Roughness{#roughness}

Surface roughness. Specifies the relative glossiness of the material surface. Used in conjunction with catalog::Type and catalog::Gloss to control 3D reflection render effects.

## Properties {#section-70c3f2394fd8477ca83a369448907971}

Integer number. Percentage value in the range 0…100. Optional for all materials. Used only for vignettes with multiple reflection maps or vignettes with 3D reflection capability. Leave empty or set to -1 if not known or not needed.

## Default {#section-c6d5c0613a8745ddbd9f43c8c90b1580}

-1; a server default is used.

## See also {#section-d08b59eb76824226b89c6fdf86bb5ce5}

[rough=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180) , [catalog::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb), [catalog::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)

