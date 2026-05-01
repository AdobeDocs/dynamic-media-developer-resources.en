---
description: Image map data. None or more complete HTML <AREA> elements, sorted front-to-back.
solution: Experience Manager
title: Map
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9490b5c-0f85-4256-8590-0d6aa52a19d5
TQID: https://experienceleague.adobe.com/fcEKrYWfdbIB9mZzD1FQXTUsihyRcqlaBV4UGlDlp9w
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
# Map{#map}

Image map data. None or more complete HTML `<AREA>` elements, sorted front-to-back.

The server interprets and may change the SHAPE and COORDS attributes (SHAPE=CIRCLE is not supported in this release). All other attributes of `<AREA>` are passed through without modification. Coordinate values specified with the COORDS attribute must be pixel offsets from the top-left corner of the unmodified source image. (`%` coordinates are not supported in this release and may not be processed correctly.)

## Properties {#section-f52d89fd399b4356ac05277e6c12f956}

Text string value. If specified, it must be one or more complete HTML `<AREA>` elements.

This field participates in text string localization. Refer to [Text String Localization](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) in the *HTTP Protocol Reference* for details.

## Default {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

None.

## See also {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) , [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [Text String Localization](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
