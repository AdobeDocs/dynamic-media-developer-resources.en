---
description: Default image mode. Selects how the default image is applied when images specified in the request are not found.
solution: Experience Manager
title: DefaultImageMode
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b30ce72f-7c74-407c-bd4a-042b84c469e9
TQID: 'https://experienceleague.adobe.com/pe73D8ZWHMpPQSfd6KEk7rh4hD-eJCBuUrHC9n-yIUw'
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
# DefaultImageMode{#defaultimagemode}

Default image mode. Selects how the default image is applied when images specified in the request are not found.

## Properties {#section-7fa8acb63540490d9f5186231b5e77c3}

Enum. '0' to replace the entire composite image, even if the missing image is just one of several layers; '1' to replace each missing layer source image with the default image and return the composite as usual.

## Restrictions {#section-04cb0d50e8914564a8d226d0d4663c8b}

Image Serving reverts back to `DefaultImageMode=0` when nested Image Rendering, FXG, or `req=set` requests fail.

## Default {#section-9e318524a2a5496386901286748c7ee7}

Inherited from `default::DefaultImage` if not defined or if empty.

## See also {#section-fddce1d27a0c43fb8b4d891f76ac5a52}

[defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433) , [attribute::DefaultImage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
