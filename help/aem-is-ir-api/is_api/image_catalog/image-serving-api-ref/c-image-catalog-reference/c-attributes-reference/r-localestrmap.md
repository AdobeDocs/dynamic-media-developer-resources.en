---
description: String translation map. Refers to a locId that can be mapped to any number of internalLocId.
seo-description: String translation map. Refers to a locId that can be mapped to any number of internalLocId.
seo-title: LocaleStrMap
solution: Experience Manager
title: LocaleStrMap
topic: Scene7 Image Serving - Image Rendering API
uuid: 388a5032-1d76-4279-8144-8fa9355c8ed4
index: y
internal: n
snippet: y
---

# LocaleStrMap{#localestrmap}

String translation map. Refers to a locId that can be mapped to any number of internalLocId.

 ` *`item`*&#42;['|' *`item`*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item </span> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> locale </span>, <span class="varname"> locId </span>*[',' <span class="varname"> locId </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locale </span> </p> </td> 
  <td class="stentry"> <p>Locale (not case sensitive). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId </span> </p> </td> 
  <td class="stentry"> <p>Internal locale ID. </p> </td> 
 </tr> 
</table>

`LocaleStrMap` refers to a `locId` that can be mapped to any number of `internalLocId`.

An empty *`locale`* value matches empty and unknown `locale=` strings. This allows defining a default rule for unknown locales.

Empty *`locId`* values are permitted and select the *`defaultString`* (the *`defaultString`* does not have a locale identifier). *`locId`* values are searched in the order specified. The first match is returned.

String translation, when enabled, is applied to text strings in the following image catalog fields: 

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>Catalog Field</b> </td> 
   <td> <b>String Element in Field</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::ImageSet </span> </p> </td> 
   <td> <p>Any sub-element containing a translatable string (delimited by any combination of separators ',' ';' ':' and/or the start/end of the field). </p> <p>A <span class="codeph"> 0xrrggbb </span> color value at the beginning of a localizable field is excluded from localization and passed through without modification. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Map </span> </p> </td> 
   <td> <p>Any single- or double-quoted attribute value, except the values of the <span class="codeph"> coords= </span> and <span class="codeph"> shape= </span> attributes. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Targets </span> </p> </td> 
   <td> <p>The value of any <span class="filepath"> target.*.label </span> and <span class="filepath"> target.*.userdata </span> property. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::UserData </span> </p> </td> 
   <td> <p>The value of any property. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-8505a8525f6948ada3979f68c4081044}

One or more items, separated with |, where each item consists of two or more, comma-separated, string values.

## See also {#section-0c0516e4f83d42d38247308cab9b6708}

Localization Support, [locale=](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleMap](../../../../../is_api/image_catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [catalog::ImageSet](r_imageset_cat.md#reference_4764D347AFD64AFDAEDE9A74C7565256), [catalog::Map](r_map_cat.md#reference_F1B52F35D07A4B3EA9E9AE1628526EEA), [catalog::Targets](r_targets_cat.md#reference_4C3865D34A34421786F2A4070955575A), [catalog::UserData](r_userdata_cat.md#reference_1E552AEAD08E41489E82EC16936BC0DF) 
