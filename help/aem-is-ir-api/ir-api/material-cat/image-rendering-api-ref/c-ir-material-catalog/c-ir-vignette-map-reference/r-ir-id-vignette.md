---
description: Vignette identifier. Index key value by which records in the vignette map file are looked up by the server.
solution: Experience Manager
title: Id
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5c0c8788-ffe5-4b42-86f6-6b4683dd7c21
TQID: 'https://experienceleague.adobe.com/qzcJRZ14-LqFm0H6ayTrFVSYNaJpv8YlPAkxaTkmNC4'
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
# Id{#id}

Vignette identifier. Index key value by which records in the vignette map file are looked up by the server.

 Typically a short and unique identifier, such as a SKU number. May also be a more complex string which might look like a file path.

## Properties {#section-267bbf34677e4401abbaf6fdce52191b}

Text string. Required. Primary index key for the vignette map table. Each `vignette::Id` value must be unique within the table and must not contain ',' characters.

## Default {#section-736d3419b19045efa00887cb595b0337}

None.

## See also {#section-19dce97a43a9461caf74ef3cdd560a3a}

[attribute::RootId](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootid.md#reference-54b42b7125824be593378c1accb70d5a)

