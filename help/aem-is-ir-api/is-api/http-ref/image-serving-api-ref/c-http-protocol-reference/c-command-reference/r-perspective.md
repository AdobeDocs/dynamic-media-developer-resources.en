---
description: Perspective transform. Apply a perspective transform to the layer source image to fill the region specified with the quadrilateral. Other areas of the layer remain transparent.
seo-description: Perspective transform. Apply a perspective transform to the layer source image to fill the region specified with the quadrilateral. Other areas of the layer remain transparent.
seo-title: perspective
solution: Experience Manager
title: perspective
uuid: b22d7b49-db08-48df-80bc-5b7237aea475
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# perspective{#perspective}

Perspective transform. Apply a perspective transform to the layer source image to fill the region specified with the quadrilateral. Other areas of the layer remain transparent.

 `perspective= *`perspQuad`*[, *`resOptions`*]`

`perspectiveN= *`perspQuadN`*[, *`resOptions`*]`

<table id="simpletable_4BD38BBF53964F7D97B9E58914C97B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuad</span> </p></td> 
  <td class="stentry"> <p>Perspective quadrilateral pixel coordinates (8 reals, separated by commas). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuadN</span> </p></td> 
  <td class="stentry"> <p>Perspective quadrilateral normalized coordinates (8 reals, separated by commas). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> resOptions</span> </p></td> 
  <td class="stentry"> <p>Resampling options (see below). </p></td> 
 </tr> 
</table>

*`perspQuad`* consists of four pixel coordinate values in the composite (or layer 0) coordinate space, which originates at the top-left corner of the composite image.

`perspQuadN` consists of four normalized coordinate values, where `0.0,0.0` corresponds to the top left corner of the composite/layer 0 image and `1.0,1.0` to the bottom right corner.

The input image is transformed so that the top-left corner of the input image maps to the first coordinate value of `perspQuad[N]`, the top-right corner to the second coordinate, the bottom-right corner to the third coordinate, and the bottom-left corner to the fourth coordinate.

>[!NOTE]
>
>`pos=` may be used to further position the transformed layer in the composite image.

The perspective quadrilateral coordinates may be located outside the composite image.

Behavior is undefined if the quadrilateral is not suitable for a perspective transform (for example, if two or more vertices coincide, if three or all vertices are on the same line, or if the quadrilateral is self-intersecting or concave).

## Quality considerations {#section-7cc9056afa614300a9b8844d39739fc3}

While the default implementation produces a reasonable compromise between quality and performance, at times it may be necessary to increase the resolution of the source image to improve sharpness or to reduce it to reduce aliasing artifacts.

If the source is an image, use `scale=` to choose a different resolution (relative to the full resolution of the image). The specified `scale=` value is rounded to the next higher PTIF resolution level. In case of a nested request source, the size of the image produced by the nested request can be adjusted to achieve the desired sharpness. For text layers, the resolution of the input image (the rendered text) is adjusted by selecting a larger size= value in conjunction with increasing the resolution specified with `textAttr=`.

*`resOptions`* allows selecting an alternative resampling algorithm. The following values are supported (case-sensitive):

<table id="table_0F20007986324E228096888ED37219C0"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Value</b> </th> 
   <th class="entry"> <b> Description</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> R1</span> </p> </td> 
   <td> <p> Nearest neighbor. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R2</span> </p> </td> 
   <td> <p> Bi-linear. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R3</span> </p> </td> 
   <td> <p> Standard super-sampling (default). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">R3T<span class="varname"> n</span></span> </p> </td> 
   <td> <p> Super-sampling with adjustable jitter (<span class="varname"> n</span> must be an integer value between 0 and 200). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-818e57df0a1b4449888543bc6af77751}

Layer command. Applies to the current layer or to layer 0 if `layer=comp`. Ignored by effect layers.

`res=` is always ignored when perspective is present in the same layer. `size=` is ignored when specified for image layers. `size=` and `res=` in layers with `perspective=` are reserved for future use.

## Default {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`, for no perspective transform.

## See also {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) , [scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065), [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d) 
