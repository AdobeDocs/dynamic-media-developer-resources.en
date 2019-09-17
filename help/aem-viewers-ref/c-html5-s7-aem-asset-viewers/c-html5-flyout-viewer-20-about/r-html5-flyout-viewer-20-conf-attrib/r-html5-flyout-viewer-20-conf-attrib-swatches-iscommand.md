---
description: null
seo-description: null
seo-title: Swatches.iscommand
solution: Experience Manager
title: Swatches.iscommand
topic: Dynamic media
uuid: a9928350-d9a9-49b0-8990-1f8b67d82f10
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

## Properties {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Default {#section-a08032f0fcf041c09e63c0238a339fc9}

None.

## Example {#section-0338be21edd04ff1a3bed5c8319b61a4}

When specified in the viewer URL:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

When specified in the configuration data:

`iscommand=op_sharpen=1&op_colorize=0xff0000` 
