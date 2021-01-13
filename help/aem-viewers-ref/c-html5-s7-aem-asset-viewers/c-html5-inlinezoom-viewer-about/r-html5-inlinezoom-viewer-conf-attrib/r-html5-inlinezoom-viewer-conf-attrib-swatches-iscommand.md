---
description: Swatches.iscommand
solution: Experience Manager
title: Swatches.iscommand
topic: Dynamic media
uuid: a7d3b93b-daa2-4d08-8e2f-52e3ea11efbd
---

# Swatches.iscommand{#swatches-iscommand}

 ` [Swatches.|<containerId>_swatches.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> The Image Serving command string that is applied to all swatches. If it is specified in the URL, be sure that you HTTP-encode all occurrences of <span class="codeph"> &amp;</span> and <span class="codeph"> =</span> as <span class="codeph"> %26</span> and <span class="codeph"> %3D</span>, respectively. </p> <p> <p>Note:  Image sizing manipulation commands are not supported. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optional.

## Default {#section-fcb06fd8e7e945e590094efcf9a1d510}

None.

## Example {#section-3a188ab955c445bcb2efa3c49722c10d}

When specified in the viewer URL.

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

When specified in the configuration data.

`iscommand=op_sharpen=1&op_colorize=0xff0000` 
