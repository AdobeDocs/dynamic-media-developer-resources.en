---
title: videoServerUrl
description: URL command for Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 2bcbe117-14a3-42c8-bdd3-790b32bb757c
TQID: https://experienceleague.adobe.com/ijyYgx8rmP5lwloB9jj7lvNN-C-SMIxyoxVgAojO-hQ
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# videoServerUrl{#videoserverurl}

URL command for Video Viewer.

 ` videoServerUrl= *`videoRootPath`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> The video server root path. If no domain is specified, the domain from which the page is served is applied instead. Standard URI path resolution applies. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Default {#section-d016470e92a74f98a18c4ab3489410a5}

`/is/content/`

## Example {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
videoServerUrl=https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna
```
