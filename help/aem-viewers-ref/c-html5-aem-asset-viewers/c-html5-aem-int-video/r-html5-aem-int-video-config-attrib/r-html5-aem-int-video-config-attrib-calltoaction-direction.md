---
title: CallToAction.direction
description: Configuration attribute for Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 2cfeeba0-3230-481c-857a-bed3fedc836c
TQID: 'https://experienceleague.adobe.com/YehjMoK88ylklqHA9ZpjPgW8xoMwhLQqR-2e73ayWRM'
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
---
# CallToAction.direction{#calltoaction-direction}

Configuration attribute for Interactive Video Viewer.

 `[CallToAction.|<containerId>_callToAction.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p> Specifies the way thumbnails fill in the view. </p> <p>Set to <span class="codeph"> left </span> to set the left-to-right fill order. </p> <p>Set to <span class="codeph"> right </span> reverses the order so that the view is filled in a right-to-left, top-to-bottom direction. </p> <p>Set to <span class="codeph"> auto </span> to have the component apply right mode when the locale is set to <span class="codeph"> "ja" </span>; otherwise, <span class="codeph"> left </span> is used. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Default {#section-71fb773f814649b2885aefee68073641}

`auto`

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
direction=right
```
