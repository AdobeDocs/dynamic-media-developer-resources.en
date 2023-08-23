---
title: network
description: Learn about using network bandwidth optimization to adjust the image quality that is served based on actual network bandwidth.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User

---
# network{#network}

Turning on Network Bandwidth automatically adjusts the image quality that is served based on actual network bandwidth. For poor network bandwidth, [DPR (Device Pixel Ratio)](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md) optimization is automatically turned off, even if it is already on.

If desired, your company can opt out of network bandwidth optimization at the individual image level by appending `network=off` to the URL of the image.

`network=on|off`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> on|off </span> </p> </td> 
  <td class="stentry"> <p>Specifies whether network bandwidth adjusts the image quality that is served based on actual network bandwidth (on), or network bandwidth optimization is turned off for no image quality adjustment.</p> </td> 
 </tr> 
</table>

Network bandwidth values are based on the detected client-side values of the bundled CDN.

## Properties



## Default

`network=off`

## Example

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3&network=on`

## See also

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md), [drp](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md), [Smart Imaging](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)