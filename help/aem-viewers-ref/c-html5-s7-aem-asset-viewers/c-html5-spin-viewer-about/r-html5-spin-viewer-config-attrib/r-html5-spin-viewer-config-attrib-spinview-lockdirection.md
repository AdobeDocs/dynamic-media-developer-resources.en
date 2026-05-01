---
title: SpinView.lockdirection
description: SpinView.lockdirection
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: e29ba926-9e0e-4ddd-9f76-408f8ab3b4ca
TQID: https://experienceleague.adobe.com/M79iTZPyxwk7Dai7WFudY0Lt8DFmyZQ7taDcK2nNX6k
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# SpinView.lockdirection{#spinview-lockdirection}

 `[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Specifies whether to allow a change in the spin direction if there is 2D spin set. </p> <p>When set to <span class="codeph"> 1 </span>, the component identifies the primary drag or swipe direction (horizontal versus vertical) at the start of the gesture. After that, it maintains that direction until the gesture ends. For example, if the user starts a horizontal spin and then decides to continue their drag gesture in a vertical direction, the component does not perform a vertical spin. Instead, it considers only the horizontal movement of the mouse or swipe. </p> <p>A value of <span class="codeph"> 0 </span> lets a user change the spin direction at any time during the gesture progress. The setting has no effect if the spin set is 1D. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
