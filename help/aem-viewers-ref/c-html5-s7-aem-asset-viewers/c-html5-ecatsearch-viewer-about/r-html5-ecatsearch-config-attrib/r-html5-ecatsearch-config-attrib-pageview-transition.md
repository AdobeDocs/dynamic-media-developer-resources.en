---
description: PageView.transition
solution: Experience Manager
title: PageView.transition
uuid: c85ad85f-a802-4f5d-9046-00171ad2d9ca
feature: "Dynamic Media Classic,Viewers,SDK/API,eCatalog Search"
role: "Developer,Business Practitioner"
---

# PageView.transition{#pageview-transition}

 [!DNL `[PageView.|<containerId>_pageView.]transition= *`time`*[, *`easing`*]`]

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> time</span></span> </p> </td> 
   <td colname="col2"> <p> Specifies the time in seconds that the animation for a single zoom step action takes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> easing</span></span> </p> </td> 
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

## Properties {#section-ebfd9162c8504666bf0e4485bf3b1383}

Optional.

## Default {#section-9f91ce6567384ab691e4d4f8a7015455}

[!DNL `0.5,0`]

## Example {#section-cb6b8793ee9946b8bf1cfddab8612db5}

[!DNL `transition=2,2`] 
