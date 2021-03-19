---
description: URL command for Video360 Viewer.
seo-description: URL command for Video360 Viewer.
seo-title: videoServerUrl
solution: Experience Manager
title: videoServerUrl
uuid: b6fa3fc3-9182-4d05-a735-e4cc0e58c3e4
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,Business Practitioner
---

# videoServerUrl{#videoserverurl}

URL command for Video360 Viewer.

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
videoServerUrl=http://s7d9.scene7.com/is/content/
```

