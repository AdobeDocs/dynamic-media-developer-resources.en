---
description: FlyoutZoomView.flyouttransition
solution: Experience Manager
title: FlyoutZoomView.flyouttransition
topic: Dynamic Media
uuid: f1a9f2bc-9a13-4980-9241-e835a0aadd2c
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

## Properties {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Default {#section-a08032f0fcf041c09e63c0238a339fc9}

`fade,1,0,1,0`

## Example {#section-0338be21edd04ff1a3bed5c8319b61a4}

`flyouttransition=slide,1,1,2,1` 
