---
description: FlyoutZoomView.highlightmode
solution: Experience Manager
title: FlyoutZoomView.highlightmode

feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,Business Practitioner
---

# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

 ` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`showtime`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> highlight|cursor </span> </p> </td> 
   <td colname="col2"> <p> Specifies the type of navigation frame to use. When set to <span class="codeph"> cursor </span>, the component uses a fixed-size reference cursor. It is possible to have different cursor art for desktop systems and touch devices, this is controlled with <span class="codeph"> .s7cursor </span> CSS class and <span class="codeph"> input=mouse|touch </span> attribute selector. On desktop systems, an anchor point is set in the middle of the cursor area, while on touch devices anchor is located in the bottom center of the cursor. When set to <span class="codeph"> highlight </span>, the component uses a variable-size navigation frame; the size and shape of the frame depends on the zoom factor and the size of the flyout view. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime </span> </span> </p> </td> 
   <td colname="col2"> <p> Sets the time (in seconds) it takes the highlight or cursor to fade in after it is activated by the user. Fade in is applied only on touch devices; on desktop systems it is ignored by the component. </p> <p>Fade in applies to the following UI elements: highlight frame, fixed cursor, overlay (in case <span class="codeph"> overlay </span> parameter is set to <span class="codeph"> 1 </span>). Flyout view animation begins only after highlight/cursor fade in animation completes. There is no fade out animation. When the user deactivates the flyout, corresponding UI elements (cursor, highlight and overlay) hide instantly. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|free </span> </p> </td> 
   <td colname="col2"> <p> Controls navigation frame positioning. </p> <p>If set to <span class="codeph"> onimage </span> the navigation frame can only be positioned inside the actual image area within the main view. </p> <p>If set to <span class="codeph"> free </span> a user can move the navigation frame anywhere in the logical main view area, even outside image content. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Default {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## Example {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free` 
