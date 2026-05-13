---
title: Size
description: Decal size. Width, height, and thickness of a decal material object.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 964cb4c1-5256-40eb-94ea-761916174b79
TQID: 'https://experienceleague.adobe.com/HLyEmmOch9kiHQ3sqpvHCQiHOBltjQcsZaDu0na1-Ww'
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
# Size{#size}

Decal size. Width, height, and thickness of a decal material object.

## Properties {#section-967bf1112eec4032a91ed0c8a7b10a07}

Three real numbers separated by commas. It must not be negative. Set unused values to 0. Trailing zeros may be omitted.

Specify both width and height only if the image should be stretched to fit the specified size (the aspect ratio may change). Set either width or height to scale the image proportionally. Set both width and height to 0 to use `catalog::Resolution`to determine the object size.

Provide a thickness value to add a drop shadow to the decal object. Optional for decal materials, ignored by all other materials.

## Default {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

0,0,0. This indicates that the decal size is to be determined based on catalog::Resolution, and that the object does not have a thickness (therefore, no drop shadow is rendered).

## Examples {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>The decal is forced to 12x3 inches in size and has no thickness (this is, no drop shadow). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>The decal is 5 inches wide, the height is determined by the aspect ratio of the image, and a drop shadow is rendered based on a 1-inch thickness. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,.5 </p></td> 
  <td class="stentry"> <p>The decal width and height is determined by catalog::Resolution, and that it is ½ inch thick. </p></td> 
 </tr> 
</table>

## See also {#section-31a164e781d14e92bd9d379d3c329e92}

[catalog::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
