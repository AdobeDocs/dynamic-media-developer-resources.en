---
description: FlyoutZoomView.iscommand
solution: Experience Manager
title: FlyoutZoomView.iscommand

feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: b23918b5-5fc6-4038-b6f5-519198a96f86
---
# FlyoutZoomView.iscommand{#flyoutzoomview-iscommand}

 ` [FlyoutZoomView.|<containerId>_flyout.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> </p> <p>The Image Serving command string that is applied to the FlyoutZoomView main image and the zoomed in view. If it is specified in the URL, be sure that you HTTP-encode all occurrences of <span class="codeph"> &amp;</span> and <span class="codeph"> =</span> as <span class="codeph"> %26</span> and <span class="codeph"> %3D</span>, respectively. </p> <p> <p>Note:  Image sizing manipulation commands are not supported. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Default {#section-a08032f0fcf041c09e63c0238a339fc9}

None.

## Example {#section-0338be21edd04ff1a3bed5c8319b61a4}

When specified in the viewer URL:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

When specified in the configuration data:

`iscommand=op_sharpen=1&op_colorize=0xff0000`
