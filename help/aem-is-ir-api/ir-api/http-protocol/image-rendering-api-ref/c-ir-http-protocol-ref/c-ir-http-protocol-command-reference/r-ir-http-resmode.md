---
description: Resampling mode. Selects the resampling and/or interpolation algorithm to be used for scaling the rendered image to the size specified with wid=, hei=, or scl=.
seo-description: Resampling mode. Selects the resampling and/or interpolation algorithm to be used for scaling the rendered image to the size specified with wid=, hei=, or scl=.
seo-title: resMode
solution: Experience Manager
title: resMode
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 106da74a-d7da-4998-a719-c4c69ae36f6b
---

# resMode{#resmode}

Resampling mode. Selects the resampling and/or interpolation algorithm to be used for scaling the rendered image to the size specified with wid=, hei=, or scl=.

 ` `resMode=bilin|bicub|sharp2|bisharp``

<table id="table_AF954C101B30473FAFE9930C7B694305"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bilin </span> </p> </td> 
   <td colname="col2"> <p>Selects standard bilinear interpolation. Fastest resampling method; some aliasing artifacts may be noticeable. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bicub </span> </p> </td> 
   <td colname="col2"> <p>Selects bicubic interpolation. More CPU-intensive than bilinear interpolation, but will yield sharper images with less noticeable aliasing artifacts. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> sharp2 </span> </p> </td> 
   <td colname="col2"> <p>Selects a modified Lanczos Window function as an interpolation algorithm. May produce slightly sharper results than bicubic at a higher CPU cost. </p> <p> <span class="codeph"> sharp </span> has been replaced by <span class="codeph"> sharp2 </span>, which has a lesser likelihood of causing aliasing artifacts, also known as Moiré. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bisharp </span> </p> </td> 
   <td colname="col2"> <p>Selects the <span class="keyword"> Adobe Photoshop </span> default resampler for reducing image size which is called "bicubic sharper" in <span class="keyword"> Adobe Photoshop </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-ea7029f37e094d9cb85646b85fbac0ce}

May occur anywhere within the request. Ignored if no final image scaling is applied.

## Default {#section-900872fb93dc41efb3e8ad5b62aadc38}

`attribute::ResMode`

## See also {#section-16c557a2250e4f04b3e6cbef18add9ce}

[attribute::ResMode](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-resmode.md#reference-fdca7eb6d5104fdeae9d6ac42251db82) , [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29) 
