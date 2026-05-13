---
title: op_saturation
description: Adjust saturation. Changes the saturation of each visible pixel of the layer or composite image.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cd71e27e-6ccc-4ade-9bcf-af8e41bcf381
TQID: 'https://experienceleague.adobe.com/lTgjlQNmfVcS1XswABjicGEHjDUO1PVjM7wD1Zi6o2M'
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
# op_saturation{#op-saturation}

Adjust saturation. Changes the saturation of each visible pixel of the layer or composite image.

 `op_saturation= *`adj`*`

<table id="simpletable_5F118A28FE674B06A16F6F19C56B4594"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Saturation adjustment (-100…+100 int). </p></td> 
 </tr> 
</table>

`op_saturation=-100` fully desaturates the image.

## Properties {#section-9a3cc9ff060049449554dfa69d92fd53}

Layer command. Applies to the current layer or to the composite image if `layer=comp`. Ignored by effect layers.

## Default {#section-ef0e78f55c8b4d22aee09104dad6410a}

`op_saturation=0`, for no change in saturation. CMYK images or layers are converted to RGB before the operation is applied.

## Example {#section-033b272f1b7e4efeb94e841fd8095357}

Manipulate a color photograph so you can achieve a "high-key" appearance:

`http://server/myRootId/myImageId?op_saturation=-60&op_brightness=45&op_contrast=-35`
