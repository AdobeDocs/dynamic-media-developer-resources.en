---
description: Image Set. Specifies an image set value for use when generating req=set response.
seo-description: Image Set. Specifies an image set value for use when generating req=set response.
seo-title: imageSet
solution: Experience Manager
title: imageSet
uuid: ecfb3905-e3ef-4ab8-a2c4-2c3f200e0f0f
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# imageSet{#imageset}

Image Set. Specifies an image set value for use when generating req=set response.

 `imageSet=val`

<table id="simpletable_F697691D166C407D82233664814F4663"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Image set string. </p></td> 
 </tr> 
</table>

To escape the value and ensure that any included modifiers are not interpreted as being part of the URL query string, the entire value should be enclosed in curly braces. If the catalog record is specified in the net path, this modifier value overrides `catalog::ImageSet` from the main record. For a description of valid image set syntax, refer to `catalog::ImageSet` documentation.

## Properties {#section-66e7bb7bf4664cbcac6f7ebb2f0d3a4f}

Request attribute. Optional. Overrides `catalog::ImageSet` from main record.

## Default {#section-e8622ff40408450fb79d028f8d37fa6b}

None.

## Example {#section-68513d3c601f477399602a0741dab390}

Specify image set for use with `req=set` request:

`http://server/myRootId?imageSet={asset1,asset2,asset3}&req=set`

## See also {#section-7e0320b2e09d475897082711a8f023a9}

[catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md) , [req=set](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Media Set Requests](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-media-set-requests.md#reference-f2f2aa11208b47609fe17848d3b86a0b) 
