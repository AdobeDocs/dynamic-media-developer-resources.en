---
description: FlyoutZoomView.flyouttransition
solution: Experience Manager
title: FlyoutZoomView.flyouttransition
uuid: 0b94956d-9ee6-409e-9b52-29c888932a0e
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,Business Practitioner
---

# FlyoutZoomView.flyouttransition{#flyoutzoomview-flyouttransition}

 ` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *`showtime`*[, *`showdelay`*[, *`hidetime`*[, *`hidedelay`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|slide|fade </span> </span> </p> </td> 
   <td colname="col2"> <p> Specifies the type the effect applied when the flyout view is shown or hidden. With <span class="codeph"> none </span>, the flyout image appears instantly when activated and ready; <span class="codeph"> slide </span> makes the slide animation play in left-to-right direction; <span class="codeph"> fade </span> applies an alpha transition to the flyout image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime </span> </span> </p> </td> 
   <td colname="col2"> <p> Number of seconds that the show animation takes to complete. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showdelay </span> </span> </p> </td> 
   <td colname="col2"> <p> The delay in seconds between user action which initiates the show animation and the beginning of show animation itself. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hidetime </span> </span> </p> </td> 
   <td colname="col2"> <p> Number of seconds that the hide animation takes to complete. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hidedelay </span> </span> </p> </td> 
   <td colname="col2"> <p> The delay in seconds between user action which initiates the hide animation and the beginning of hide animation itself. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optional.

## Default {#section-fcb06fd8e7e945e590094efcf9a1d510}

`fade,1,0,1,0`

## Example {#section-3a188ab955c445bcb2efa3c49722c10d}

`flyouttransition=slide,1,1,2,1` 
