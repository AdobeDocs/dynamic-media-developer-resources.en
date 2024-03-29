---
title: Swatches.iscommand
description: Swatches.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 3336c4d2-0d1d-4c6f-8163-8a84a8be8c20
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

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

None.

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

When specified in the viewer URL.

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

When specified in the configuration data.

`iscommand=op_sharpen=1&op_colorize=0xff0000`
