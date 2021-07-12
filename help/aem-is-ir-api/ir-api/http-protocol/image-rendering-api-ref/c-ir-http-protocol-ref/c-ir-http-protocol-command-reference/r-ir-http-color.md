---
description: Foreground color. Specifies the color of solid color materials or the additive color for colorizable materials.
solution: Experience Manager
title: color
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6086a7ca-d3cf-4cec-967b-83347293ea0a
---
# color{#color}

Foreground color. Specifies the color of solid color materials or the additive color for colorizable materials.

 `color= *`color`*`

<table id="simpletable_C5AF9074CCA64EA5921772DF3F7E0F55"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> color</span> </p> </td> 
  <td class="stentry"> <p>RGB or gray color value. </p></td> 
 </tr> 
</table>

## Properties {#section-629c3c91221c48c4b7f7b31a13fd1766}

Material attribute. Required for solid color materials, optional for all other materials.

## Default {#section-ea8e1967674d426bb8f46abe365b6aca}

`catalog::Color` if the material is based on a catalog entry. Otherwise, `none` for no colorizing.

## See also {#section-5eb8f1c36634474bbfaa63d84e4c3c71}

[catalog::Color](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-color.md#reference-7639487fe0ac48beb9e8afa4dc845552) , [bgc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-bgc.md#reference-3f5c78cea01c4a85aa582076d23aebb0)
