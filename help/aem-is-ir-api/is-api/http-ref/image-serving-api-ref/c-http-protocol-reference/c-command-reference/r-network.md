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

DPR and network bandwidth values are based on the detected client-side values of the bundled CDN. These values are sometimes inaccurate. For example, iPhone5 with `dpr=2`, and iPhone12 with `dpr=3`, both show `dpr=2`. Still, for high-resolution devices, sending `dpr=2` is better than sending dpr=1. The best way to overcome this inaccuracy, however, is to use client-side DPR to give you 100% accurate values. And it works for any device, whether it is Apple or any other device that was launched. See [Use Smart Imaging with client-side Device Pixel Ratio](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/client-side-dpr.html?lang=en).

## Properties



## Default

`network=off`

## Example

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3&network=on`

## See also

[drp](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md), [Smart Imaging](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)