---
description: Region-of-interest. Specifies a rectangular region-of-interest (ROI) in the composite image, expressed in pixels.
seo-description: Region-of-interest. Specifies a rectangular region-of-interest (ROI) in the composite image, expressed in pixels.
seo-title: rgn
solution: Experience Manager
title: rgn
topic: Scene7 Image Serving - Image Rendering API
uuid: 08657925-c52a-4279-8357-c26ad5c5ef3d
---

# rgn{#rgn}

Region-of-interest. Specifies a rectangular region-of-interest (ROI) in the composite image, expressed in pixels.

rgn= *`coord`*, *`size`*

<table id="simpletable_3A430F9078B04C2E90F4D1A130AFA20C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>Pixel offset from the top-left corner of the composite image to the top-left of the ROI (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> size</span> </p></td> 
  <td class="stentry"> <p>Size of the ROI in pixels (int, int). </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>`rgn=` only defines an ROI without cropping the image. When `wid=` and/or `hei=` larger than size are applied as well, additional data from the composite image may be visible in the final reply image.

## Properties {#section-53edb35f4e364d7ca13fd0886e8b0c86}

View attribute. Applies regardless of the current layer setting.

Any areas of the ROI extending outside the composite image are padded with `bgc=`.

`rgn=` is applied before final scaling and fitting with `scl=`, `wid=`, `hei=`, `fit=`, `rect=`, or `align=`.

## Default {#section-6a3df8f670084def900ffef9dab7e94a}

Entire composite image ( `rgn=0,0,width,height`).

## See also {#section-07883760f25c4d17aedbee36b7883891}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47), [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3) 
