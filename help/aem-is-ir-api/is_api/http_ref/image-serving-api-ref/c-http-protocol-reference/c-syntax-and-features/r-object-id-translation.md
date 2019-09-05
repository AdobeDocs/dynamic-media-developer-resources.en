---
description: Image Serving provides a mechanism to translate external object ids to locale-specific object (catalog) IDs. The primary application is for providing locale-specific content and content shared amongst multiple locales without the client application needing to know the locale-specific object IDs.
seo-description: Image Serving provides a mechanism to translate external object ids to locale-specific object (catalog) IDs. The primary application is for providing locale-specific content and content shared amongst multiple locales without the client application needing to know the locale-specific object IDs.
seo-title: Object ID translation
solution: Experience Manager
title: Object ID translation
topic: Scene7 Image Serving - Image Rendering API
uuid: 49b74b7c-7180-4ebc-9f8b-12bd15bc3c24
index: y
internal: n
snippet: y
---

# Object ID translation{#object-id-translation}

Image Serving provides a mechanism to translate external object ids to locale-specific object (catalog) IDs. The primary application is for providing locale-specific content and content shared amongst multiple locales without the client application needing to know the locale-specific object IDs.

The application can be written using only global object IDs and Image Serving will automatically substitute locale-specific images and other content where available.

The *`locale`* is specified in Image Serving requests with the `locale=` command.

>[!NOTE]
>
>Object ID translation is only applicable for catalog-based use of Image Serving. File names cannot be translated.

## Scope {#section-66fcd5bd467c4eeaa1574583cbe9756d}

All references to entries in image, SVG, and static content catalogs are considered for translation-fonts and ICC profile references are not translated. In addition to the *`object`* in the path of [!DNL /is/image] and [!DNL /is/static requests], these commands and catalog attributes are subject to ID translation: `src=`, `mask=`, `template=`, `defaultImage=`, `attribute::DefaultImage`, and `attribute::Watermark`.

## The ID translation map {#section-9e417b352c314dfe94e831fdd62cddc8}

`attribute::LocaleMap` defines the rules used by the server to determine the ID of the localized content, given as inputs the generic object ID and the `locale=` value.

`attribute::LocaleMap` consists of a list of input *locales* (matching the values specified with `locale=`), each with none or more output locale suffixes ( ` *`locSuffixes`*`).

For example, `attribute::LocaleMap` might look like this:

`en,_E,|en_us,_E,|en_uk,_E,|fr,_F,|de,_D,|de_at,_D,|de_de,_D,|,_E,`

The request `/is/image/myCat/myImg?locale=de_de` would return the image associated with the catalog entry `myCat/myImg_D` (assuming that such a catalog entry exists).

Refer to the description of `attribute::LocaleMap` for details.

## The translation process {#section-1f64db17e9f644d88e09853670e14a16}

Given the example above, the server first looks for the *`locale`* " `de_de`" in the ID translation map. It then iterates over the *`locSuffixes`* associated with this entry-in this case " `_D`" and "" (empty suffix). For each iteration, the suffix is appended to the image ID and the resulting id tested for existence in the catalog. If found, that catalog entry is used, otherwise the next one is tested. For this example, these entries are checked: `myCat/myImg_D`, and `myCat/myImg`. If no match is found, the server returns an error or a default image (if so configured).

## Unknown locales {#section-b2f3c83f2dc845d69b5908107b775537}

In the above example, `attribute::LocaleMap` includes an empty *`locale`* which defines the default translation rule, used for unknown `locale=` values (i.e. those not explicitly listed in the translation map). If this translation map were applied to the request `/is/image/myCat/myImg?locale=ja`, it would resolve to `myCat/myImg_E`, if it exists, or otherwise `myCat/myImg`.

If a translation map does not specify a default translation rule, an error will be returned for all requests with unknown `locale=` values.

## Examples {#section-cc40bb00ee9248bb8cb23e17d7a5984c}

**Multi-tiered lookup**

It is often desirable to group locales (for example, European, Middle Eastern, North American) to address regional standards. This can be achieved with a multi-tiered lookup.

For this example, we want to support collections for Western and Middle Eastern use. Both collections are based on the generic image collection, and both add or modify some images. Both collections are then further refined for specific locales ( `m1`, `m2` for two middle-eastern variants, and `w1`, `w2`, and `w3` for three Western locales), except that images are shared for `w1` and `w3`. Unknown locales are mapped only to the generic collection and do not have access to locale-specific images.

`attribute::LocaleMap: w1,-W,|w2,-W2,-W,|w3,-W,|m1,-M1,-M,|m2,-M2,-M,|,`

The following table illustrates which catalog entries will be considered, and the order in which they are considered for the generic input ID `myImg`: 

<table id="table_97EB13E3DB9B48D3A4184D5ECC8E9F86"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>locale</i> </b> </th> 
   <th class="entry"> <b>Catalog IDs to be searched</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> w1, w3 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> w2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W2, myImg-W, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m1 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M1, myImg-M, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M2, myImg-M, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>all others </p> </td> 
   <td> <p> <span class="codeph"> myImg </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Search for specific IDs**

Some image naming conventions may not support generic image IDs internally. The generic IDs from the request must always be mapped to a specific ID in the catalog; often the exact specific ID may not be known.

For this example, images for all languages may have `_1`, `_2`, or `_3` suffix. Images specific to French locales may have `_22` or `_23` suffix, and images specific to German locales may have `_470` or `_480` suffix.

`attribute::LocaleMap: ,_1,_2,_3|fr,_22,_23,_1,_2,_3|de,_470,_480,_1,_2,_3| de_at,_470,_480,_1,_2,_3| de_de,_470,_480,_1,_2,_3`

The following table illustrates which catalog entries are considered, and the order in which they are considered for the generic input ID `myImg`: 

<table id="table_A7EE4AA0F1C24284B83CC4B40622D24F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>locale</i> </b> </th> 
   <th class="entry"> <b>Output IDs to be searched</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fr </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_22, myImg_23, myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> de </span>, <span class="codeph"> de_at </span>, <span class="codeph"> de_de </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_470, myImg_480, myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>all others </p> </td> 
   <td> <p> <span class="codeph"> myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## See also {#section-05893816c66a406d89f9bfd6ace8d47a}

[attribute::LocaleMap](../../../../../is_api/image_catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318) , [attribute::DefaultLocale](../../../../../is_api/image_catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b), [locale=](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [req=xlate](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) 
