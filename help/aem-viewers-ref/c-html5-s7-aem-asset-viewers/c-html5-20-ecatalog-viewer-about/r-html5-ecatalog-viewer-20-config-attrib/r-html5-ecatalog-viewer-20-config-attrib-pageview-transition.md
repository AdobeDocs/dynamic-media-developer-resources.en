---
title: PageView.transition
description: PageView.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: aa12a210-88d9-4b96-b598-6967496ac668
TQID: 'https://experienceleague.adobe.com/zsCMR3hoGnEbFG1wapFyvB1oKROPcgP9yifLH-wtwPQ'
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
# PageView.transition{#pageview-transition}

 ` [PageView.|<containerId>_pageView.]transition= *`time`*[, *`easing`*]`

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

`0.5,0`

## Example {#section-cb6b8793ee9946b8bf1cfddab8612db5}

`transition=2,2`

