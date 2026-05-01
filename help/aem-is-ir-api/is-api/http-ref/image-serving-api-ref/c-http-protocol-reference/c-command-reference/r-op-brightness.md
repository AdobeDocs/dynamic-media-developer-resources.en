---
title: op_brightness
description: Adjust brightness. Decreases or increases the image brightness.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 390ed812-87ae-41e7-8021-65dd95915ae8
TQID: https://experienceleague.adobe.com/kyxz9m1tH8qmcmkZJ2DNIyIJfnftWm0YSfpgR0mZi2g
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
# op_brightness{#op-brightness}

Adjust brightness. Decreases or increases the image brightness.

 `op_brightness= *`adj`*`

<table id="simpletable_2B5DB95B1FF044C8BD226D4F8311E806"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Brightness adjustment (-100…+100 int). </p></td> 
 </tr> 
</table>

## Properties {#section-c7e757f63b2c4b5ebaacbadb51c72ce4}

Layer command. Applies to the current layer or to the composite image if `layer=comp`. Ignored by effect layers. CMYK images or layers are converted to RGB before the operation is applied.

## Default {#section-be56be0759634c79b4f264f194a94dbc}

`op_brightness=0`, for no change of brightness.

## Example {#section-c25f952f1b77409abb9ccf885862d75c}

Darken the background of an image slightly to emphasize the foreground content:

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_brightness=-10&layer=1&src=myRootId/myImageId`
