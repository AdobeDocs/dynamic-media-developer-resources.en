---
description: Jpeg Size in KiloBytes. Specifies the maximum size of the JPEG response in kilobytes.
solution: Experience Manager
title: jpegSize
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# jpegSize{#jpegsize}

Jpeg Size in KiloBytes. Specifies the maximum size of the JPEG response in kilobytes.

 `jpegSize= *`size`*`

<table id="simpletable_EC2A8D8B65854B45B9CB184DA1069355"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> size</span></span> </p> </td> 
  <td class="stentry"> <p>Size in kilobytes. </p></td> 
 </tr> 
</table>

If this is set to a positive value, and if the JPEG response with the specified JPEG quality does not exceed this value, that image is returned as the response. Otherwise, the JPEG quality decreases until it either produces an image which fits in to the specified size or until it determines it cannot fit. In the latter case, the request fails with an error.

A value of 0 means that the response is not constrained by size.

Negative values are not allowed.

## Properties {#section-19e544e77d35478b98fe8666f27d6968}

Request attribute. Applies regardless of current layer setting. Ignored if the output image format is not JPEG.

## Default {#section-198b798ed187453197e0969c641d6fb5}

0

## Example {#section-46bf806fd3ef4875b7726df32b6f834d}

Guarantee size is not too large for delivering to a device with limited memory:

`http://server/myRoodId/myImageId?qlt=60&wid=300&jpegSize=10`

## See also {#section-98d472b39d6547969fce6dd86748c153}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [attribute::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09) 
