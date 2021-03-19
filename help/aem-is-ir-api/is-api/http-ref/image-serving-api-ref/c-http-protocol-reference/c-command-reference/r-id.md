---
description: Image/Metadata Version. When working with content that changes frequently, servers in caching networks such as Akamai, browser caches, and corporate proxy server caches may store Image Serving responses which may be out of date for periods of time.
seo-description: Image/Metadata Version. When working with content that changes frequently, servers in caching networks such as Akamai, browser caches, and corporate proxy server caches may store Image Serving responses which may be out of date for periods of time.
seo-title: id
solution: Experience Manager
title: id
uuid: 3d526326-c8fa-4aef-95a9-93ccacf08f73
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Business Practitioner"
---

# id{#id}

Image/Metadata Version. When working with content that changes frequently, servers in caching networks such as Akamai, browser caches, and corporate proxy server caches may store Image Serving responses which may be out of date for periods of time.

 ` id= *`val`*`

<table id="simpletable_3A6EBDA15B004636804E1ACEF952479A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> val </span> </span> </p> </td> 
  <td class="stentry"> <p>Version string. </p> </td> 
 </tr> 
</table>

Image Serving includes a versioning mechanism which can help reduce the chance that an outdated cache entry is used by an application. This mechanism involves using `req=props` to obtain version identifier strings for image data and metadata (such as image map or zoom target data). The version identifier string is then added to cacheable Image Serving requests with the `id=` command.

When a source image or metadata changes, the corresponding version id value will also change. Including an up-to-date version id value with the `id=` command ensures that old cache entries will no longer be accessed.

The following table lists the version identifier strings to be used for each `req=` type: 

<table id="table_AE39BEBE18864880BBBF1C4F16785E2D"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> req= type</b> </th> 
   <th class="entry"> <b> version identifier from req=props</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> img </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> map </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> mask </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> targets </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> tmb </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> userdata </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> xmp </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
 </tbody> 
</table>

`req=` types not listed above either have a short TTL ( `attribute::NonImgExpiration`) or their responses are not cacheable at all; there is no advantage to including `id=` with such requests.

## Properties {#section-62e973d0d5884abebbb0679f9278ae2c}

Request attribute. Optional. Always ignored by the server.

## Default {#section-96136720c82842c89505347ec39e6024}

None.

## Example {#section-a5fb871e0ec8485c91c4fca78895d17f}

See the description of [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3) for example usage.

## See Also {#section-6b4befb47202415195a68516f60e9988}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) , [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3), [catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a), [attribute::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d) 
