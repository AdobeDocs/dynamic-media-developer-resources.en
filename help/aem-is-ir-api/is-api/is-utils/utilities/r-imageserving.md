---
description: Image Serving control script. This script is used to start, stop, or restart the Image Serving Server Supervisor, which in turn starts, stops, or restarts all other Image Serving components.
solution: Experience Manager
title: ImageServing
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 252e12d9-703e-4fbb-a156-8dcdc3bc4f2e
TQID: 'https://experienceleague.adobe.com/KyiS-GblbCE-Q4Exrdz8T1W5thFn9cHellB-1-QYZaw'
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
# ImageServing{#imageserving}

Image Serving control script. This script is used to start, stop, or restart the Image Serving Server Supervisor, which in turn starts, stops, or restarts all other Image Serving components.

## Usage {#section-6832b5b10404442a9d3a3eca92041002}

` ImageServing *`command`*`

## Commands {#section-90436a0b0f70435f9ac42dafeed2c17b}

<table id="table_692C6A043F9747C88929FF20373EC88C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Command </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> start </span> </p> </td> 
   <td colname="col2"> <p> Start the Server Supervisor and all other Image Serving components. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> stop </span> </p> </td> 
   <td colname="col2"> <p> Stop all Image Serving components, including the Server Supervisor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> restart </span> </p> </td> 
   <td colname="col2"> <p>Restart all Image Serving components, including the Server Supervisor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> restart { ps | is | svg } </span> </p> </td> 
   <td colname="col2"> <p> Restarts Tomcat/[!DNL Platform Server], the Image Server, or SVG. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> status [ ps | is | svg ] </span> </p> </td> 
   <td colname="col2"> <p>Returns uptime and current memory usage information for the Image Server, Tomcat/[!DNL Platform Server], and SVGserver, or status for just the specified sever; an informational message is returned instead if the Server Supervisor is not running. </p> </td> 
  </tr> 
 </tbody> 
</table>
