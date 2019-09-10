---
description: Decal size. Width, height, and thickness of a decal material object.
seo-description: Decal size. Width, height, and thickness of a decal material object.
seo-title: Size
solution: Experience Manager
title: Size
topic: Scene7 Image Serving - Image Rendering API
uuid: 07d41f71-e18d-4559-afc7-75dc1c45be93
index: y
internal: n
snippet: y
---

# Size{#size}

Decal size. Width, height, and thickness of a decal material object.

## Properties {#section-967bf1112eec4032a91ed0c8a7b10a07}

Three real numbers separated by commas. Must not be negative. Set unused values to 0. Trailing zeros may be omitted.

Specify both width and height only if the image should be stretched to fit the specified size (the aspect ratio may change). Set either width or height to scale the image proportionally. Set both width and height to 0 to use `catalog::Resolution`to determine the object size.

Provide a thickness value to add a drop shadow to the decal object. Optional for decal materials, ignored by all other materials.

## Default {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

0,0,0. This indicates that the decal size is to be determined based on catalog::Resolution, and that the object does not have a thickness (thus no drop shadow will be rendered).

## Examples {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>The decal is forced to 12x3 inches in size and has no thickness (this is, no drop shadow). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>The decal is 5 inches wide, the height is determined by the aspect ratio of the image, and a drop shadow is rendered based on a 1 inch thickness. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,.5 </p></td> 
  <td class="stentry"> <p>The decal width and height is determined by catalog::Resolution, and that it is ½ inch thick. </p></td> 
 </tr> 
</table>

## See also {#section-31a164e781d14e92bd9d379d3c329e92}

[catalog::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806) 
