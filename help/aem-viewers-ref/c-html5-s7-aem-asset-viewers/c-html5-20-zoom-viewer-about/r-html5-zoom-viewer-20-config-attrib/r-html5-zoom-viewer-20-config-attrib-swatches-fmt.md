---
description: null
seo-description: null
seo-title: Swatches.fmt
solution: Experience Manager
title: Swatches.fmt
topic: Dynamic media
uuid: 61e6372c-bab9-4aac-a8a1-dffecc2e4903
---

# Swatches.fmt{#swatches-fmt}

 `[Swatches.|<containerId>_swatches.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_4620F51BD77149FDB68F1FBECC443801"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td> <p>Specifies the image format that the component uses for loading images from Image Server. If the specified format ends with <span class="codeph"> -alpha</span>, the component renders images as transparent content. For all other image formats the component treats images as opaque. Note that the component has a white background by default. Therefore, to make the background transparent set the <span class="codeph"> background-color</span> CSS property to <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Default {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt-png-alpha` 
