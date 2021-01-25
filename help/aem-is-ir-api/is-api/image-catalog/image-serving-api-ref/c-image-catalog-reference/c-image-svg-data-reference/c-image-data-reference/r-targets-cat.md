---
description: Zoom target data. None or more zoom target properties, which may be used in conjunction with the zoom viewer client.
seo-description: Zoom target data. None or more zoom target properties, which may be used in conjunction with the zoom viewer client.
seo-title: Targets
solution: Experience Manager
title: Targets
topic: Dynamic Media Image Serving - Image Rendering API
uuid: ca02483a-9aa0-4b54-b6f0-4fd10d8b2b4c
---

# Targets{#targets}

Zoom target data. None or more zoom target properties, which may be used in conjunction with the zoom viewer client.

The server returns the content of this field in response to `req=targets`, after replacing ' `??`' record terminator tokens.

Up to four properties may be associated with each zoom target:

` Target. *`num`*.frame= *`frame`*`

` Target. *`num`*.rect= *`left,top,width,height`*`

` Target. *`num`*.label= *`label`*`

` Target. *`num`*.userData= *`userData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> num </span> </span> </p> </td> 
  <td class="stentry"> <p>Zoom target number (int); zoom targets must be numbered sequentially and consecutively, starting with 1. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> frame </span> </span> </p> </td> 
  <td class="stentry"> <p>Optional frame/page number for targeting a specific frame/page of a spin or brochure set; defaults to 0 if not specified for spin and brochure viewer use; ignored by the zoom viewer. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> left, top </span> </span> </p> </td> 
  <td class="stentry"> <p>Pixel offset from the top-left of the image to the top-left of the zoom target rectangle (int, int); must be 0 or greater. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width, height </span> </span> </p> </td> 
  <td class="stentry"> <p>Pixel size of the zoom target rectangle (int, int); must be greater than 0. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> label </span> </span> </p> </td> 
  <td class="stentry"> <p>Text data value; may be used as a text label for a zoom target link. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> userData </span> </span> </p> </td> 
  <td class="stentry"> <p>Text data value; may be used to pass target-specific information to the client, such as a SKU value or hot-link URL. </p> </td> 
 </tr> 
</table>

Target. *`num`*.rect is required for each zoom target and must specify a rectangle fully within the image. All other properties are optional.

*`label`* and *`userData`* participate in text string localization. Refer to [Text String Localization](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) in the *HTTP Protocol Reference* for details.

For applications involving the spin and brochure viewer clients, the zoom targets must be defined in the same catalog record that defines the image set. Any zoom target definitions in the catalog records of the members of the image set are ignored by the viewer.

The Dynamic Media viewers expect zoom targets in the coordinates of the full-resolution image already adjusted by the commands from `catalog::Modifier`.

## Properties {#section-b3f8eba4985f4b00bb935d592fe770f9}

[Property data](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) value.

## Default {#section-feab29f6575e482391086a57f547543c}

None.

## See also {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catalog::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) , [catalog::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834), [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [Text String Localization](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) 
