---
title: SpinView.sensitivity
description: SpinView.sensitivity
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 256cffae-d284-4f46-a2dc-4618ea7eda57
TQID: 'https://experienceleague.adobe.com/B19x2Bn3GNq8YFUo-0HiSbyBQ4qrMcONvRSN1tNqOg0'
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
# SpinView.sensitivity{#spinview-sensitivity}

 ` [SpinView.|<containerId>_spinView.]sensitivity= *`xSensitivity`*[, *`ySensitivity`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> xSensitivity</span>[, <span class="varname"> ySensitivity</span>]</span> </p> </td> 
   <td colname="col2"> <p> Controls the sensitivity of the horizontal and vertical spin performed with a mouse drag or swipe. </p> <p> <span class="codeph"> xSensitivity</span> sets how many full horizontal product rotations are made if the user drags their mouse horizontally from one side of the view to the other. For example, three means that the user sees three complete spins for one full drag gesture. </p> <p>Likewise, <span class="codeph"> ySensitivity</span> controls the sensitivity of the vertical spin. A value of 1 means that one full vertical drag or swipe changes the view angle from the top-most spin plane to the bottom-most (or conversely). </p> <p>Setting a negative value for <span class="codeph"> ySensitivity</span> reverses the direction of the vertical spin. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
