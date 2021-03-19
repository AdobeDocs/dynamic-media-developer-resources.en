---
description: SearchPanel.fmt
solution: Experience Manager
title: SearchPanel.fmt
uuid: 58b88cc9-e07a-47aa-a0d2-c81428ca4d1e
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
---

# SearchPanel.fmt{#searchpanel-fmt}

 [!DNL `[SearchPanel.|<containerId>_searchPanel.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`]

<table id="table_8629FDB399124A57B8026E46687D0BC2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Specifies the image format that the component uses for loading images from Image Server. It can be any format supported by Image Server and the client browser. </p> <p>If the specified format ends with <span class="codeph"> -alpha</span>, the component renders images as transparent content. For all other image formats the component treats images as opaque. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-12a6fb2fcbc1476b95bd53ce880dc185}

Optional.

## Default {#section-4b6a350501124ffa9a6b1b71b32eff5d}

[!DNL `jpeg`]

## Example {#section-7de29e43bb3640e4aa1f8984b4afddad}

[!DNL `fmt=png-alpha`] 
