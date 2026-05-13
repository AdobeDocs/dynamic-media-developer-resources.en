---
title: InteractiveSwatches.scrollstep
description: Configuration attribute for Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 15bf7af8-428b-4c1c-b7ad-004563347d7c
TQID: 'https://experienceleague.adobe.com/28KSiSs54nPSMOpQm7thVn5We8EBvmyAN-YHQB-aITA'
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
# InteractiveSwatches.scrollstep{#interactiveswatches-scrollstep}

Configuration attribute for Interactive Video Viewer.

 ` [InteractiveSwatches.|<containerId>_interactiveSwatches.]scrollstep= *`step`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> step</span></span> </p> </td> 
   <td colname="col2"> <p>Specifies the number of swatches to scroll for each tap of the corresponding scroll button. </p> <p>If the specified value is greater than the number of interactive swatches visible, each tap only scrolls by the number of visible swatches to prevent the omission of any swatch. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Default {#section-71fb773f814649b2885aefee68073641}

`3`

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
scrollstep=1
```
