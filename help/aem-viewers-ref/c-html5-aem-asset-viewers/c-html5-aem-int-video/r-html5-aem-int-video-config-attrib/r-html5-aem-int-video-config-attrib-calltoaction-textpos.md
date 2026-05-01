---
title: CallToAction.textpos
description: Configuration attribute for Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: f2356eb1-2f71-49b6-bb40-6cd332e6785b
TQID: https://experienceleague.adobe.com/JaJ4ojuSmCzF2V5Fy3FMcu8ZqNSwxbogic-FJOiCEjw
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# CallToAction.textpos{#calltoaction-textpos}

Configuration attribute for Interactive Video Viewer.

 `[CallToAction.|<containerId>_callToAction.]textpos=bottom|top|left|right|none|tooltip`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom|top|left|right|none|tooltip</span> </p> </td> 
   <td colname="col2"> <p> Specifies where the label is drawn relative to the thumbnail image. That is, the label is centered at the specified location relative to the thumbnail. </p> <p>When <span class="codeph"> tooltip</span> is specified, the label text is displayed as a floating tooltip over the thumbnail image. </p> <p>Set to <span class="codeph"> none</span> to turn off the label. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Default {#section-71fb773f814649b2885aefee68073641}

`bottom`

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
textpos=top
```
