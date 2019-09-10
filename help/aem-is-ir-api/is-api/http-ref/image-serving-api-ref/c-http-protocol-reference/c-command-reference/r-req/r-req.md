---
description: Request type. Specifies the type of request.
seo-description: Request type. Specifies the type of request.
seo-title: req
solution: Experience Manager
title: req
topic: Scene7 Image Serving - Image Rendering API
uuid: b888be10-89e5-4b41-a2bd-f83533ea2481
index: y
internal: n
snippet: y
---

# req{#req}

Request type. Specifies the type of request.

 `req={catalogprops|exists|imageprops|imageset|img|loadcache|map|mask|mbrSet|message|props|resolve|saveToFile|set|targets|tmb|userdata|validate|xlate|xmp}[, *`options`*]`

<table id="simpletable_E8556552FA204665A0B1B03EFD8CAC70"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> options</span></span> </p> </td> 
  <td class="stentry"> <p>See detailed description of each request type. </p></td> 
 </tr> 
</table>

Unless otherwise noted in the detailed descriptions, the server will return `text` responses with MIME type `text/plain`. Many request types let you specify a response type, such as `text`, that is typically the default, `javascript`, `xml`, or `json`. The associated response MIME types are `text/plain`, `text/javascript`, `text/xml`, and `text/javascript`, respectively.

Unless otherwise noted, responses format the response as a set of `name=value` pairs.

See [Properties](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9). 
