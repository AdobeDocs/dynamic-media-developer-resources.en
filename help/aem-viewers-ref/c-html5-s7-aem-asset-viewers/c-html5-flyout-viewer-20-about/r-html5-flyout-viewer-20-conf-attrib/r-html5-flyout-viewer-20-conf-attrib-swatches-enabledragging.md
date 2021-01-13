---
description: Swatches.enabledragging
solution: Experience Manager
title: Swatches.enabledragging
topic: Dynamic media
uuid: 2b5dff77-25e3-42cd-bdae-0a96f04f881e
---

# Swatches.enabledragging{#swatches-enabledragging}

 ` [Swatches.|<containerId>_swatches.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td> <p> Enables or disables the ability for a user to scroll the swatches with a mouse or by using touch gestures </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue </span> </span> </p> </td> 
   <td> <p> Functions within the <span class="codeph"> 0-1 </span> range. It is a <span class="codeph"> % </span> value for movement in the wrong direction of the actual speed. If it is set to <span class="codeph"> 1 </span>, it moves with the mouse. If it is set to <span class="codeph"> 0 </span>, it does not let you move in the wrong direction at all. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Default {#section-a08032f0fcf041c09e63c0238a339fc9}

`1,0.5`

## Example {#section-0338be21edd04ff1a3bed5c8319b61a4}

`enabledragging=0` 
