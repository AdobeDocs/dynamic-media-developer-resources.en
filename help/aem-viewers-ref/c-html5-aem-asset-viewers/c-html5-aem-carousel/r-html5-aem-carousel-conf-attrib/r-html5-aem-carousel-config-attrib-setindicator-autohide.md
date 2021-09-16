---
title: SetIndicator.autohide
description: SetIndicator.autohide
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 75521239-a0be-4aa0-b65d-9a1f7d902cf2
---
# SetIndicator.autohide{#setindicator-autohide}

` [SetIndicator.|<containerId>_setIndicator.]autohide=0|1[, *`limit`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">0|1[,<span class="varname"> limit</span>]</span> </p> </td> 
   <td colname="col2"> <p> Configures auto-hide behavior depending on number of pages and run-time component size. </p> <p> <span class="codeph"> 0</span> turns off the auto-hide. </p> <p> <span class="codeph"> 1</span> enables the auto-hide. The component hides its dots if at least one of the following conditions turns true: </p> <p> 
     <ul id="ul_A7F9C1DDC6AE44BAA348B3AD440A4EDD"> 
      <li id="li_39332158806445DF874C5A52F1331B8B">the row with dots becomes wider than the run-time component width, or </li> 
      <li id="li_E30BAC8B609147ADB8824000F5729B21">number of pages set for this component exceeds the limit configured by the <span class="codeph"><span class="varname"> limit</span></span> parameter. </li> 
     </ul> </p> <p> Setting <span class="codeph"><span class="varname"> limit</span></span> to <span class="codeph"> -1</span> disables the second auto-hide condition. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Default {#section-71fb773f814649b2885aefee68073641}

`1,10`

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

`autohide=0`
