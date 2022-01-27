---
title: ZoomView.iscommand
description: ZoomView.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: faa6344a-a0b5-4b27-818b-81e9e0b721b4
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

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

None.

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

When specified in the viewer URL:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

When specified in the config data:

`iscommand=op_sharpen=1&op_colorize=0xff0000`
