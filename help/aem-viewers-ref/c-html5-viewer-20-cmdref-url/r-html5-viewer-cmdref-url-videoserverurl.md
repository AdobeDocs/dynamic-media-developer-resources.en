---
title: videoServerUrl
description: Parameter common to all viewers.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: db0ce8c4-3754-4fef-9430-44ee8e5c5e80
TQID: https://experienceleague.adobe.com/bTILjqqVxQEfoNBsHFbJCxTESIoRuvYZ7WCbD1kaXFc
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

Parameter common to all viewers.

>[!NOTE]
>
>This command does not apply to Video Image Viewer.

` videoServerUrl= *`videoRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> The video server root path. If no domain is specified, then the domain from which the page is served is applied instead. Standard URI path resolution applies. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-10ee45d637134e0fbcd943c62578cb78}

Optional. Not needed for standard software as a service usage.

## Default {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/content/`

## Example {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
videoServerUrl=http://s7d1.scene7.com/is/content/
```
