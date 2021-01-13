---
description: Swatches.enabledragging
solution: Experience Manager
title: Swatches.enabledragging
topic: Dynamic media
uuid: f676b0b1-2ce0-4409-8db6-ce162b03053b
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

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,0.5`

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enabledragging=0` 
