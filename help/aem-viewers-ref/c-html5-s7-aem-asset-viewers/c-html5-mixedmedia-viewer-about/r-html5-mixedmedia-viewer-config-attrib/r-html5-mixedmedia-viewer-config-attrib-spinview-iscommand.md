---
description: null
seo-description: null
seo-title: SpinView.iscommand
solution: Experience Manager
title: SpinView.iscommand
topic: Dynamic media
uuid: e2c86ec3-0f8a-42eb-98a1-689f083fa20c
---

# SpinView.iscommand{#spinview-iscommand}

 ` [SpinView.|<containerId>_spinView.]iscommand= *`isCommand`*`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> The Image Serving command string that is applied to spin image. If specified in the URL all occurrences of <span class="codeph"> &amp;</span> and <span class="codeph"> =</span> must be HTTP-encoded as <span class="codeph"> %26</span> and <span class="codeph"> %3D</span>, respectively. </p> <p> <p>Note:  Image sizing manipulation commands are not supported. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

None.

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

When specified in the viewer URL:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

When specified in the config data:

`iscommand=op_sharpen=1&op_colorize=0xff0000` 
