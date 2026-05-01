---
title: icc
description: Output color profile.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39b25f7c-ed3c-4132-8241-e7f3aab07b00
TQID: https://experienceleague.adobe.com/lNMkld1amVW4JFSdBHWJ9QpCQqvgCrKSqMPVUy-YS0Q
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
# icc{#icc}

Output color profile.

icc= *`profile`*[, *`renderIntent`*[, *`blackpointComp`*]]

<table id="simpletable_DF1914FD351E4F2BA61372A52F0CFFBF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> profile</span></span> </p></td> 
  <td class="stentry"> <p>ICC color profile. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent </span> </span> </p></td> 
  <td class="stentry"> <p>perceptual | relative | saturation | absolute </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span> </span> </p></td> 
  <td class="stentry"> <p>1 to enable, 0 to disable blackpoint compensation. </p></td> 
 </tr> 
</table>

*`profile`* Specifies the output color space profile to which the rendered image should be converted if it is different from the working profile. *`profile`* Must be either a valid `icc::Name` defined in the ICC profile map of an image catalog or default catalog, or a relative path to a profile file (typically with [!DNL `.icc`] or [!DNL `.icm`] suffix).

>[!NOTE]
>
>*`profile`* May not include ',' characters, even if HTTP-encoded.

*`renderIntent`* Allows overriding the default rendering intent.

*`blackpointComp`* Enables blackpoint compensation if the output profile supports this feature.

>[!NOTE]
>
>Not all color conversions support all *`renderIntent`* and *`blackpointComp`* choices. Typically, these settings are honored only when the ICC output profile characterizes an output device such as a printer or monitor. Also, some ICC output profiles do not support all *`renderIntent`* choices.

## Properties {#section-b4042623a8ea40248c11b2153e5906b1}

May occur anywhere within the request. An error is returned if the image type is specified with `fmt=` does not match *`profile`*.

Both *`renderIntent`* and *`blackpointComp`* are ignored if not compatible with the specified ICC profile.

CMYK output device profiles are more likely to support different rendering intents.

## Default {#section-bbd3206fdcac4dc48a08fc9eba14fc90}

If color management is enabled and `icc=` is not specified, the server delivers the image converted to the output profile ( `attribute::IccProfile*`) matching the image type specified with `fmt=`.

If not specified, *`renderIntent`* is inherited from `attribute::IccRenderIntent`, and *`blackpointComp`* is inherited from `attribute::IccBlackPointCompensation`.

## See also {#section-37ef83149fd74345956a98f633cc0294}

[Color Management](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-color-management.md#concept-7bac7c2c41be42c1b301eae80abe6b8d), [attribute::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127), [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f), [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)
