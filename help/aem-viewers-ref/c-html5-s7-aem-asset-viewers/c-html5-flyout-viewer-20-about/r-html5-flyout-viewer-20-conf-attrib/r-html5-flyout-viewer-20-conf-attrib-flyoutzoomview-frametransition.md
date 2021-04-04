---
description: FlyoutZoomView.frametransition
solution: Experience Manager
title: FlyoutZoomView.frametransition

feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,Business Practitioner
exl-id: 0b0a88a0-d736-4ab8-a25f-15d1689b0a48
---
# FlyoutZoomView.frametransition{#flyoutzoomview-frametransition}

` [FlyoutZoomView.|<containerId>_flyout.]frametransition=none|fade[, *`duration`*]`

<table id="table_FC34B37AACFB4E92A37E1D2D93D5F0D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Specifies the type of the effect applied to main view on asset change. The <span class="codeph"> none</span> stands for no transition, main view change happens instantly. The <span class="codeph"> fade</span> activates cross-fade transition where the old image fades out and the new image fades in </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duration</span></span> </p> </td> 
   <td colname="col2"> <p> Number of seconds that the animation takes to complete. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Default {#section-a08032f0fcf041c09e63c0238a339fc9}

None.

## Example {#section-0338be21edd04ff1a3bed5c8319b61a4}

`frametransition=fade,1`
