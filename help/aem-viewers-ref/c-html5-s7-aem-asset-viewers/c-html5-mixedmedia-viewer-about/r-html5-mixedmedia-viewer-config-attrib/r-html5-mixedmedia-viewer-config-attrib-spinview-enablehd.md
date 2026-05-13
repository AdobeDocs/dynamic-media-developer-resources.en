---
title: SpinView.enableHD
description: SpinView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0a2abdc6-eae5-4dda-b749-599cd8a07a98
TQID: 'https://experienceleague.adobe.com/sVDq51PMMpTHbeBjGsIM3WS2p-Ap1ifJOBLiMylzrek'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
---
# SpinView.enableHD{#spinview-enablehd}

 ` [SpinView.|<containerId>_spinView.]enableHD=always|never|limit[, *`number`*]`

<table id="table_8929B59833DE4E1C89FA4BCF07309809"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Enable, limit, or disable optimization for devices where <span class="codeph"> devicePixelRatio</span> is greater than <span class="codeph"> 1</span>, that is devices with a high-density display like iPhone4 and similar devices. If active then the component limits the size of the IS image request as if the device only had a pixel ratio of <span class="codeph"> 1</span> and therefore reducing the bandwidth. </p> </td> 
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
