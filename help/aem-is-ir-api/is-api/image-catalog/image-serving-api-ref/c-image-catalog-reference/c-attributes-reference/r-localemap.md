---
description: ID translation map. Specifies the rules used for translating generic image ids to locale-specific IDs.
solution: Experience Manager
title: LocaleMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c1d74154-721b-46cc-9f0b-8dae5647b179
TQID: 'https://experienceleague.adobe.com/LqHo03WC7EWKP7jt4l1X6kJffXcOQSd8unCxbdjOig4'
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
# LocaleMap{#localemap}

ID translation map. Specifies the rules used for translating generic image ids to locale-specific IDs.

 `*`item`*&#42;['|' *`item`*]`

<table id="simpletable_A6DD1A28F8ED4178A8ADDB2F3AEFC402"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> item</span> </p></td> 
  <td class="stentry"> <p><span class="varname"> locId</span>,<span class="varname"> locSuffix</span>*[','<span class="varname"> locSuffix</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locId</span> </p></td> 
  <td class="stentry"> <p>Locale ID (not case-sensitive). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locSuffix</span> </p></td> 
  <td class="stentry"> <p>Locale suffix. </p></td> 
 </tr> 
</table>

`LocaleMap` refers to a `locId` that can be mapped to any number of `locSuffix`.

Empty *`locSuffix`* values are permitted. *`locSuffix`* values must be sorted in the order in which they are to be searched. The first match is returned.

Image Serving searches the *`locId`* values for a case-insensitive match with the `locale=` value specified in the request. If a match is found, the first associated *`locSuffix`* value is appended to the original catalog id. If this catalog entry exists it is used, otherwise the next *`locSuffix`* value is tried. If none of the *`locSuffix`* values matches a catalog entry, Image Serving returns an error or a default image.

An empty *`locId`* value matches empty and unknown `locale=` strings. This allows defining a default rule for unknown locales.

ID translation, when enabled, is applied to all ids referencing image catalog and static contents catalog entries.

## Properties {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

One or more items, separated with |, where each item consists of two or more, comma-separated string values. *`locId`* and `locale=` are compared. Not case-sensitive.

## See also {#section-19fba6d5be59439c8bf8ec7513c1a6da}

Localization Support, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
