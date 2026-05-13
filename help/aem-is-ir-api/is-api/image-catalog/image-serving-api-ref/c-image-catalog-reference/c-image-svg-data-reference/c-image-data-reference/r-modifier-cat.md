---
description: Prefix request modifier string. None or more Image Serving commands separated by '&' characters.
solution: Experience Manager
title: Modifier
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6eef3159-c082-469b-b9dc-29acb28560d6
TQID: 'https://experienceleague.adobe.com/b1j5WmY-PNOt1zW9qglJob5W8csmI3TidhDwoHK3kCM'
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
# Modifier{#modifier}

Prefix request modifier string. None or more Image Serving commands separated by '&' characters.

 Used to persistently modify images and store the body of templates.

Commands in this field are overridden by the same commands in the request or template from which this record is referenced, and by commands in `catalog::PostModifier`

Macros are permitted in `catalog::Modifier`, as long as they are defined in the same catalog or in the default catalog. Custom variables may be used as well.

## Properties {#section-6674388f77d644469371a17e8809c45f}

Text string. Optional.

## Default {#section-f4ffe8b75792435c8b1040e75c5fb8a1}

None.

## See also {#section-7a67803d141b442180c418c1f3cff029}

[catalog::PostModifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md#reference-4bc3738a812b4e7c8a180e27bfbd770b)
