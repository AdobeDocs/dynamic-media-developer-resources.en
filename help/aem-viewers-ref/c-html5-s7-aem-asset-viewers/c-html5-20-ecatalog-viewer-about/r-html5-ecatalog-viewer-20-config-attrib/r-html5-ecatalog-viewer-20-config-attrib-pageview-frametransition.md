---
description: PageView.frametransition
solution: Experience Manager
title: PageView.frametransition
uuid: feeb02c0-f3f9-4559-acd9-cad30788b70b
feature: "Dynamic Media Classic,Viewers,SDK/API,eCatalog"
role: "Developer,Business Practitioner"
---

# PageView.frametransition{#pageview-frametransition}

 ` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`duration`*]`

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slide|turn|auto</span> </p> </td> 
   <td colname="col2"> <p> Specifies the type of effect that is applied on frame change. </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> slide</span> activates a transition where the old frame slides out of view and the new frame slides in to view. </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> turn</span> enables a page flip effect, when a user can drag one of the four spread corners and perform an interactive page flip. </p> <p>When <span class="codeph"> turn</span> is used the appearance of the component is controlled with the <span class="codeph"> pageturnstyle</span> modifier and the <span class="codeph"> .s7pagedivider</span> CSS class is ignored. </p> <p>Note:  <p><span class="codeph"> turn</span> animation is not supported on Motorola Xoom. </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> auto</span> sets the turn frame transition on desktop systems and the slide transition on touch devices. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duration</span></span> </p> </td> 
   <td colname="col2"> <p>Specifies the duration in seconds of a <span class="codeph"> slide</span> or <span class="codeph"> turn</span> transition effect. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-4d25a3f483834d2b9586fa70270ce6bd}

Optional.

## Default {#section-d677f04f1c894966884ce9d77a5ea1c1}

`slide,0.3`

## Example {#section-b877011e5f6240718e9451be8f622c02}

`frametransition=auto,1` 
