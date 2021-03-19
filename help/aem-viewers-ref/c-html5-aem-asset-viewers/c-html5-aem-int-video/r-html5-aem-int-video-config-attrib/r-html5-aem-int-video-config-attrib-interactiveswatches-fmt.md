---
description: Configuration attribute for Interactive Video Viewer.
seo-description: Configuration attribute for Interactive Video Viewer.
seo-title: InteractiveSwatches.fmt
solution: Experience Manager
title: InteractiveSwatches.fmt
uuid: 0a30c913-39d1-4521-b65c-f2b3879f6928
feature: "Dynamic Media Classic,Viewers,SDK/API,Interactive Videos"
role: "Developer,Business Practitioner"
---

# InteractiveSwatches.fmt{#interactiveswatches-fmt}

Configuration attribute for Interactive Video Viewer.

 `[InteractiveSwatches.|<containerId>_interactiveSwatches.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Specifies the image format that the component uses for loading images from Image Server. </p> <p>If the specified format ends with "<span class="codeph"> -alpha</span>", the component renders the images as transparent content. For all other image formats the component treats the images as opaque. Note that the component has a white background by default. Therefore, to make it completely transparent set the <span class="codeph"> background-color</span> CSS property to <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Default {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
fmt=png-alpha
```

