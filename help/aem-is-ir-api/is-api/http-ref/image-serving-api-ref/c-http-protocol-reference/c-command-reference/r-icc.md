---
description: Output Color Profile.
seo-description: Output Color Profile.
seo-title: icc
solution: Experience Manager
title: icc
uuid: cfbd18aa-cbba-4085-920d-1f54645d0f89
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# icc{#icc}

Output Color Profile.

 `icc= *`object`*[, *`renderIntent`*[, *`blackpointComp`*[, *`dither`*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> object</span> </span> </p></td> 
  <td class="stentry"> <p>ICC color profile. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> perceptual|relative|saturation|absolute</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1 to enable, 0 to disable blackpoint compensation. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> dither</span></span> </p></td> 
  <td class="stentry"> <p>1 to enable, 0 to disable dithering. </p></td> 
 </tr> 
</table>

*`object`* specifies the output color space profile to which the image should be converted if it is different than the working profile. *`profile`* must be either a valid `icc::Name` defined in the ICC profile map of an image catalog or default catalog, or a relative path to a profile file (typically with [!DNL .icc] or [!DNL .icm] suffix). See [ *`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) for additional information.

>[!NOTE]
>
>*`object`* may not include ',' characters, even if HTTP-encoded.

*`renderIntent`* allows overriding the default rendering intent.

*`blackpointComp`* enables blackpoint compensation if the output profile supports this feature.

>[!NOTE]
>
>Not all color conversions support all *`renderIntent`* and *`blackpointComp`* choices. Typically, these settings are honored only when the ICC output profile characterizes an output device such as a printer or monitor. Also, some ICC output profiles do not support all *`renderIntent`* choices.

Note

*`dither`* enables dithering (actually error diffusion), which may avoid or reduce color banding artifacts.

## Properties {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

Request attribute. The server will return an error if an image type is specified with `fmt=` which does not match *`profile`*.

*`renderIntent`* and *`blackpointComp`* are ignored if not compatible with the specified ICC profile. CMYK output device profiles are more likely to support different rendering intents.

## Default {#section-0b9fe2eb428447df8ae9948f11ab5aae}

If color management is enabled and `icc=` is not specified, the server will deliver the image converted to the output profile ( `attribute::IccProfile*`) matching the image type specified with `fmt=`.

If not specified, *`renderIntent`* is inherited from `attribute::IccRenderIntent`, *`blackpointComp`* is inherited from `attribute::IccBlackPointCompensation`, and *`dither`* is inherited from `attribute::IccDither`.

## See also {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[attribute::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [attribute::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a), [object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [Color Management](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7), [ICC Profile Map Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e) 
