---
title: jpegSize
description: Jpeg Size in KiloBytes. Specifies the maximum size of the JPEG response in kilobytes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08cecb09-100f-4671-b335-d59c88b0e1ef
TQID: https://experienceleague.adobe.com/UiUdqY2Yjy2DMOLp-Y3SZ5WDrjZdaKjBDYaw-g60sM0
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
