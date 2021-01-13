---
description: ImageMapEffect.rollover
solution: Experience Manager
title: ImageMapEffect.rollover
topic: Dynamic media
uuid: 276122d8-2109-42eb-be13-bead35cd3fe2
---

# ImageMapEffect.rollover{#imagemapeffect-rollover}

[!DNL `[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`]

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p>Specifies when to display the info panel. </p> <p>If set to <span class="codeph"> 1</span>, the info panel is displayed when the mouse enters image map area (in case the image map has non-empty, <span class="codeph"> rollover_key</span> attribute). </p> <p>If set to <span class="codeph"> 0</span> info panel is triggered when the image map is clicked (if the image map has a non-empty <span class="codeph"> rollover_key</span> and empty <span class="codeph"> href</span> attributes). </p> <p> Ignored on touch devices, including touch-enabled desktop systems, and is automatically set to <span class="codeph"> 0</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-ccfedc2da28f412a86d03f390db92b4b}

Optional.

## Default {#section-79eb39c444814c9398df1f5f3730d289}

[!DNL `0`]

## Example {#section-b548ed09b52b4b65888ac891af08d725}

[!DNL `rollover=1`] 
