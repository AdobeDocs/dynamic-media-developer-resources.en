---
description: PageView.fmt
solution: Experience Manager
title: PageView.fmt

feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 690aed79-c242-402d-86c0-470a91fbb034
---
# PageView.fmt{#pageview-fmt}

 [!DNL `[PageView.|<containerId>_pageView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`]

<table id="table_8629FDB399124A57B8026E46687D0BC2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Specifies the image format that the component uses for loading images from Image Server. If the specified format ends with <span class="codeph"> -alpha</span>, the component renders images as transparent content. For all other image formats the component treats images as opaque. The component has a white background by default. Therefore, to make it transparent, set the <span class="codeph"> background-color</span> CSS property to <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-12a6fb2fcbc1476b95bd53ce880dc185}

Optional.

## Default {#section-4b6a350501124ffa9a6b1b71b32eff5d}

[!DNL `jpeg`]

## Example {#section-7de29e43bb3640e4aa1f8984b4afddad}

[!DNL `fmt=png-alpha`]
