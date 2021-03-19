---
description: FlyoutZoomView.frametransition
solution: Experience Manager
title: FlyoutZoomView.frametransition
uuid: c9cd5df1-fb7b-4acb-afc1-a62b563d8654
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,Business Practitioner
---

# FlyoutZoomView.frametransition{#flyoutzoomview-frametransition}

` [FlyoutZoomView.|<containerId>_flyout.]frametransition=none|fade[, *`duration`*]`

<table id="table_FC34B37AACFB4E92A37E1D2D93D5F0D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> </p> <p> Specifies the type of the effect applied to main view on asset change. </p> <p><span class="codeph"> none</span> stands for no transition, main view change happens instantly. </p> <p><span class="codeph"> fade</span> activates cross-fade transition where the old image fades out and the new image fades in </p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duration</span></span> </p> </td> 
   <td colname="col2"> <p> Number of seconds that the animation takes to complete. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optional.

## Default {#section-fcb06fd8e7e945e590094efcf9a1d510}

None.

## Example {#section-3a188ab955c445bcb2efa3c49722c10d}

`frametransition=fade,1` 
