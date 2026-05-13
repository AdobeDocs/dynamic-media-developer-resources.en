---
title: locale
description: Translation Locale Id. Specifies the locale id for the request.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d937dfa5-95dd-49fd-ac23-e77e07b0642c
TQID: 'https://experienceleague.adobe.com/VTRopZpc1aMPvWk3QRd0XyAVf-y782AVidiSDiuYdKM'
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
# locale{#locale}

Translation Locale Id. Specifies the locale id for the request.

 `locale=[ *`locId`*]`

<table id="simpletable_C1899AD02C984ED3896B7620916637E7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> locId</span></span> </p> </td> 
  <td class="stentry"> <p>Locale ID (string). </p></td> 
 </tr> 
</table>

Using this id and the rules specified with `attribute::LocaleMap` and `attribute::LocaleStrMap`, Image Serving applies optional catalog id translation and string localization.

## Properties {#section-1854a9902b884d9b8e8e713b6635723f}

Request command. Applies to the entire request, including nested/embedded requests, regardless of where it is specified. `locId` must include only printable ASCII characters. Ignored if no localization maps are defined in the main catalog of this request. An error is returned if empty or invalid `locId` is specified and no default rule is defined in `attribute::DefaultLocale`.

## Default {#section-9699fbc26de6453e9029e0003c79a7ef}

`attribute::DefaultLocale` is used when locale= is not specified.

## See also {#section-28a586d43ac4429d98e318a580c92af4}

[attribute::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b) , [attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e), Localization Support
