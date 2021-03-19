---
description: SpinView.enableHD
solution: Experience Manager
title: SpinView.enableHD
uuid: 3e7cdb44-4366-4e84-a6c7-c1cf1f5e6344
feature: "Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets"
role: "Developer,Business Practitioner"
---

# SpinView.enableHD{#spinview-enablehd}

 ` [SpinView.|<containerId>_spinView.]enableHD=always|never|limit[, *`number`*]`

<table id="table_8929B59833DE4E1C89FA4BCF07309809"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Enable, limit or disable optimization for devices where <span class="codeph"> devicePixelRatio</span> is greater than <span class="codeph"> 1</span>, that is devices with a high-density display like iPhone4 and similar devices. If active then the component limits the size of the IS image request as if the device only had a pixel ratio of <span class="codeph"> 1</span> and therefore reducing the bandwidth. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> number</span></span> </p> </td> 
   <td colname="col2"> <p> If using the <span class="codeph"> limit</span> setting, the component enables high pixel density only up to the specified limit. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`limit,1500`

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enableHD=always` 
