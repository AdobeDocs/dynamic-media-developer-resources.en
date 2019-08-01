---
description: null
seo-description: null
seo-title: SpinView.sensitivity
solution: Experience Manager
title: SpinView.sensitivity
topic: Dynamic media
uuid: 7c63a7c5-ac75-485d-94ac-d1e133fbe44f
index: y
internal: n
snippet: y
---

# SpinView.sensitivity{#spinview-sensitivity}

 ` [SpinView.|<containerId>_spinView.]sensitivity= *`xSensitivity`*[, *`ySensitivity`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> xSensitivity</span>[, <span class="varname"> ySensitivity</span>]</span> </p> </td> 
   <td colname="col2"> <p> Controls the sensitivity of the horizontal and vertical spin performed with a mouse drag or swipe. </p> <p> <span class="codeph"> xSensitivity</span> sets how many full horizontal product rotations are made if the user drags their mouse horizontally from one side of the view to the other. For example, three means that the user sees three complete spins for one full drag gesture. </p> <p>Likewise, <span class="codeph"> ySensitivity</span> controls the sensitivity of the vertical spin. A value of 1 means that one full vertical drag or swipe changes the view angle from the top-most spin plane to the bottom-most (or vice versa). </p> <p>Setting a negative value for <span class="codeph"> ySensitivity</span> reverses the direction of the vertical spin. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2` 
