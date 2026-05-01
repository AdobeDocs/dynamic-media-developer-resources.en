---
title: Swatches.align
description: Swatches.align
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 4f25112b-9e51-4a0e-9500-1b5ab0f4de87
TQID: https://experienceleague.adobe.com/ehlAWfRsak05W7lqhbBEk77JD30SXhjeR3AX5xp2kz8
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# Swatches.align{#swatches-align}

 `[Swatches.|<containerId>_swatches.]align=left|center|right,top|center|bottom`

Specifies the internal alignment (anchoring) of the swatches container within the component area. In Swatches, the internal thumbnail container is sized so that only a whole number of swatches is shown. As a result, there is some padding between internal container and external component bounds. This command specifies how the internal swatches container is positioned inside component.

<table id="table_58D88FF5F83A4ABA928695B5AFF97354"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> left|center|right</span> </p> </td> 
   <td> <p> Sets the alignment of the horizontal swatches. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><span class="codeph"> top|center|bottom</span> </p> </td> 
   <td> <p> Sets the alignment of the vertical swatches. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`center,center`

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`align=left,top`
