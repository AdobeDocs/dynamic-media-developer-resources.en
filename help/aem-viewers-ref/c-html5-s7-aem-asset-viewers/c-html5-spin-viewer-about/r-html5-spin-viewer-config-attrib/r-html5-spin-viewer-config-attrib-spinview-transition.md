---
description: SpinView.transition
solution: Experience Manager
title: SpinView.transition

feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,Business Practitioner
---

# SpinView.transition{#spinview-transition}

 ` [SpinView.|<containerId>_spinView.]transition= *`time`*[, *`easing`*]`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> time</span></span> </p> </td> 
   <td colname="col2"> <p> Specifies the time in seconds that the animation for a single zoom step action takes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> easing</span></span> </p> </td> 
   <td colname="col2"> <p> Creates an illusion of acceleration or deceleration which makes the transition appear more natural. You can set easing to one of the following: </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0 (auto) </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1 (linear) </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2 (quadratic) </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3 (cubic) </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4 (quartic) </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5 (quintic) </li> 
     </ul> </p> <p>Auto mode always uses linear transition when elastic zoom is disabled (default). Otherwise, it fits one of the other easing functions based on the transition time. That is, the shorter the transition time the higher the easing function is used to accelerate the acceleration or deceleration effect. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-924163cb2f6542499f49894becef7fb5}

Optional.

## Default {#section-7a2128fd488941948aff18421f533ccf}

`0.5,0`

## Example {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`transition=2,2` 
