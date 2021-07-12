---
description: Default render image size. The server constrains reply images to be no larger than this width and height, if the request does not specify the view size explicitly using wid= or hei=.
solution: Experience Manager
title: DefaultPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d60f2b8c-5213-42ad-8ec9-7e7797d74e09
---
# DefaultPix{#defaultpix}

Default render image size. The server constrains reply images to be no larger than this width and height, if the request does not specify the view size explicitly using wid= or hei=.

## Properties {#section-9dc5474fc75842308796ab6440b29611}

Two integer numbers, 0 or larger, separated by a comma. Width and height in pixels. Either or both values may be set to 0 to keep them unconstrained.

Not applicable to nested/embedded requests.

## Default {#section-1935781c561e4679aa87a5bcced8df90}

Inherited from `default::DefaultPix` if not defined or if empty.

## See also {#section-d28f18d29ef14692b8706ca08e754f54}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)
