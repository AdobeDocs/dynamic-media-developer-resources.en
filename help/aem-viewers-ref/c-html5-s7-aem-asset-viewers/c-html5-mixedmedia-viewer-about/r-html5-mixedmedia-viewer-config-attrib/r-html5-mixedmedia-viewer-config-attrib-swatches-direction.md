---
title: Swatches.direction
description: Swatches.direction
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: bd01ff03-fea7-42ad-aa99-72273f55bda0
---
# Swatches.direction{#swatches-direction}

 `[Swatches.|<containerId>_swatches.]direction=auto|left|right`

<table id="table_B4B930A32C0742F4932BF071B9EEA9F4"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td> <p> Specifies the way swatches fill in the view. </p> <p> <span class="codeph"> left </span> sets left-to-right fill order; </p> <p> <span class="codeph"> right </span> reverses the order so that the view is filled in from right-to-left, and top-to-bottom. </p> <p>When <span class="codeph"> auto </span> is set, the component applies <span class="codeph"> right </span> mode when locale is set to <span class="codeph"> ja </span>; otherwise, left is used. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`direction=right`
