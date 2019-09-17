---
description: Translation Locale Id. Specifies the locale id for the request.
seo-description: Translation Locale Id. Specifies the locale id for the request.
seo-title: locale
solution: Experience Manager
title: locale
topic: Scene7 Image Serving - Image Rendering API
uuid: 82acc0bb-fd94-44c9-8ff9-3b9cefab4627
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
