---
title: navigation
description: URL command for Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 0b42d354-2ef7-4255-8a71-c9bb9b496afd
TQID: 'https://experienceleague.adobe.com/DM5Q5HWyplX57njifMgKOVpcNga-9rykCDb3Qvz5-bY'
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
# navigation{#navigation}

URL command for Video Viewer.

 ` navigation= *`file`*`

The viewer supports video chapter navigation by way of hosted WebVTT files. Cue positioning operators are not supported.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file</span> </span> </p> </td> 
   <td colname="col2"> <p> Specifies a URL or path to WebVTT navigation content. Image Serving should host the WebVTT file. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Default {#section-d016470e92a74f98a18c4ab3489410a5}

None.

## Example {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
navigation=Scene7SharedAssets/adobe_qbc_final_nc
```
