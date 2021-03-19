---
description: URL command for Video Viewer.
seo-description: URL command for Video Viewer.
seo-title: videoServerUrl
solution: Experience Manager
title: videoServerUrl
uuid: d5542745-d7e6-42e7-8177-12184b9f2e7b
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,Business Practitioner
---

# videoServerUrl{#videoserverurl}

URL command for Video Viewer.

 ` videoServerUrl= *`videoRootPath`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> The video server root path. If no domain is specified, then the domain from which the page is served is applied instead. Standard URI path resolution applies. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-f42369774e2740dcb399626a0e4e930e}

Optional. Not needed for standard SaaS usage.

## Default {#section-d016470e92a74f98a18c4ab3489410a5}

`/is/content/`

## Example {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
videoServerUrl=http://s7d1.scene7.com/is/content/
```

