---
title: op_colorbalance
description: Adjust color balance. Adjusts the value of each RGB color component separately.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 93476778-97b0-4ad5-b22a-093239e845f0
TQID: 'https://experienceleague.adobe.com/etLnTD-hMe5kOnvak7n47O0XwOWvqtC5av4FkYZpaGI'
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
# op_colorbalance{#op-colorbalance}

Adjust color balance. Adjusts the value of each RGB color component separately.

 `op_colorbalance= *`redAdj`*, *`greenAdj`*, *`blueAdj`*`

<table id="simpletable_BBDAA6FE9A0E48E3BD8304BDED776713"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> redAdj</span> </p></td> 
  <td class="stentry"> <p>Red component adjustment (-100…+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> greenAdj</span> </p></td> 
  <td class="stentry"> <p>Green component adjustment (-100…+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> blueAdj</span> </p></td> 
  <td class="stentry"> <p>Blue component adjustment (-100…+100 int). </p></td> 
 </tr> 
</table>

Gray and CMYK input image data is converted to RGB using naive conversion which is not accurate when color management is enabled.

## Properties {#section-dff9c934f7c1442bbd02379b688d82e2}

Layer command. Applies to the current layer or to the composite image if `layer=comp`. Ignored by effect layers. CMYK images and layers are converted to RGB before the operation is applied.

## Default {#section-08d84ef715964f7daea86f5ef237d199}

`op_colorbalance=0,0,0` for no change in colors.

## Example {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

Push the color balance towards red:

… `&op_colorBalance=100,0,0&`…
