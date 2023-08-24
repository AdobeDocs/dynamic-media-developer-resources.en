---
title: dpr
description: Device Pixel Ratio (DPR)&mdash;also known as CSS pixel ratio&mdash;is the relation between a device's physical pixels and logical pixels.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User

---
# dpr{#dpr}

Device Pixel Ratio (DPR)&mdash;also known as CSS pixel ratio&mdash;is the relation between a device's physical pixels and logical pixels. Especially with the advent of retina screens, the pixel resolution of modern mobile devices is growing at a fast rate.

Enabling Device Pixel Ratio optimization renders the image at the native resolution of the screen which makes it sharp.

Currently, the pixel density of the display comes from Akamai CDN header values.

`dpr=off|on,dprValue`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> off </span> </span> </p> </td> 
  <td class="stentry"> <p>Turn off DPR optimization at an individual image URL level. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> on, dprValue </span> </span> </p> </td> 
  <td class="stentry"> <p>Override the DPR value detected by Smart Imaging, with a custom value (as detected by any client-side logic or other means). Permitted value for dprValue is any number greater than 0. </p> </td> 
 </tr> 
</table>


You can use `dpr=on,dprValue` even if the company level DPR setting as off.

Owing to DPR optimization, when the resultant image is greater than the MaxPix Dynamic Media setting, MaxPix width is always recognized by maintaining the image's aspect ratio.

| Requested image size | DPR value | Delivered image size |
|-|-|-|
|816 x 500 | 1 | 816 x 500 | 
|816 x 500 | 2 | 1632 x 1000 |
|816 x 500 | 3 | 2448 x 1500 |
|816 x 500 | 4 | 3264 x 2000 |

DPR values are based on the detected client-side values of the bundled CDN. These values are sometimes inaccurate. For example, iPhone5 with `dpr=2`, and iPhone12 with dpr=3, both show `dpr=2`. Still, for high-resolution devices, sending `dpr=2` is better than sending `dpr=1`. The best way to overcome this inaccuracy, however, is to use client-side DPR to give you 100% accurate values. And it works for any device, whether it is Apple or any other device that was launched. See [Use Smart Imaging with client-side Device Pixel Ratio](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/client-side-dpr.html?lang=en).

## Properties

A request attribute. It has no effect if `dpr` is off or if `dprValue=1`.

## Default

`dpr=off`


## Example

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3`


## See also

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md), [network](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-network.md), [Smart Imaging](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)