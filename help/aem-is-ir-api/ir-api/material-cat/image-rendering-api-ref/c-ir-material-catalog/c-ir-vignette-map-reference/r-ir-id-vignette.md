---
description: Vignette identifier. Index key value by which records in the vignette map file are looked up by the server.
solution: Experience Manager
title: Id
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 5c0c8788-ffe5-4b42-86f6-6b4683dd7c21
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
