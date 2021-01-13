---
description: ZoomView.iscommand
solution: Experience Manager
title: ZoomView.iscommand
topic: Dynamic media
uuid: 35c40a49-5b8e-443e-947a-5d91286ae214
---

# ZoomView.iscommand{#zoomview-iscommand}

 ` [ZoomView.|<containerId>_zoomView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> The Image Serving command string that is applied to zoom image. If specified in the URL all occurrences of <span class="codeph"> &amp;</span> and <span class="codeph"> =</span> must be HTTP-encoded as <span class="codeph"> %26</span> and <span class="codeph"> %3D</span>, respectively. </p> <p> <p>Note:  Image sizing manipulation commands are not supported. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Default {#section-71fb773f814649b2885aefee68073641}

None.

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

When specified in the viewer URL:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

When specified in the config data:

`iscommand=op_sharpen=1&op_colorize=0xff0000` 
