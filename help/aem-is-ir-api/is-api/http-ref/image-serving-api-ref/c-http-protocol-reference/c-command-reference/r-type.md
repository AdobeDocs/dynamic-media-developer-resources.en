---
description: Static content type filter. Specifies a filter string for static content delivered via /is/content.
solution: Experience Manager
title: type
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 9015d5f4-e42c-43e0-af85-fc9c278448e7
---
# type{#type}

Static content type filter. Specifies a filter string for static content delivered via /is/content.

 `type= *`val`*`

<table id="simpletable_B66354A826434A678F3DBC686A0F1436"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Type filter string. </p></td> 
 </tr> 
</table>

The server will compare val with the value of `catalog::Type` of the requested static content item. The item is returned to the client if the values match (case-sensitive), otherwise an error is returned.

## Properties {#section-529b088434a44a9f86a64ef548d2925b}

Only supported for static content (non-image) requests served via. Ignored if `catalog::Type` is empty or not defined.

## Default {#section-e9e8f51d0a01452183ccb510efd87d46}

No type matching is applied if `type=` is not specified or is empty.

## See also {#section-da60777a46a74f1bbfa5b2f3b240eb0f}

[Serving Static (Non-Image) Contents](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-serving-static-non-image-content.md#reference-cbe50e697fdf4c7bbb0084f98b7739da), [catalog:::UserType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-usertype-cat.md)
