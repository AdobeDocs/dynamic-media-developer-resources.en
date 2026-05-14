---
title: ImageMapEffect.rollover
description: ImageMapEffect.rollover
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 29ca3d4d-6953-4148-9b1e-01e94d1da7df
TQID: 'https://experienceleague.adobe.com/V5KPk6tOhMcCUtL7iraaeBNt4xp81Uo7FTpT-1Z44ks'
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
# ImageMapEffect.rollover{#imagemapeffect-rollover}

[!DNL `[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`]

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p>Specifies when to display the info panel. </p> <p>If set to <span class="codeph"> 1</span>, the info panel is displayed when the mouse enters the image map area (in case the image map has a non-empty, <span class="codeph"> rollover_key</span> attribute). </p> <p>If set to <span class="codeph"> 0</span>, the info panel is triggered when the image map is selected (if the image map has a non-empty <span class="codeph"> rollover_key</span> and empty <span class="codeph"> href</span> attributes). </p> <p> Ignored on touch devices, including touch-enabled desktop systems, and is automatically set to <span class="codeph"> 0</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-ccfedc2da28f412a86d03f390db92b4b}

Optional.

## Default {#section-79eb39c444814c9398df1f5f3730d289}

[!DNL `0`]

## Example {#section-b548ed09b52b4b65888ac891af08d725}

[!DNL `rollover=1`]
