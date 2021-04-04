---
description: Adjust brightness. Decreases or increases the image brightness.
solution: Experience Manager
title: op_brightness
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 390ed812-87ae-41e7-8021-65dd95915ae8
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
