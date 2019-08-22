---
description: Image Serving control script. This script is used to start, stop, or restart the Image Serving Server Supervisor, which in turn starts, stops, or restarts all other Image Serving components.
seo-description: Image Serving control script. This script is used to start, stop, or restart the Image Serving Server Supervisor, which in turn starts, stops, or restarts all other Image Serving components.
seo-title: ImageServing
solution: Experience Manager
title: ImageServing
topic: Scene7 Image Serving - Image Rendering API
uuid: 45f609dd-f41c-4b2c-9955-c1a696dcecbd
index: y
internal: n
snippet: y
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
   <td colname="col2"> <p> Restarts Tomcat/Platform Server, the Image Server, or SVG. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> status [ ps | is | svg ] </span> </p> </td> 
   <td colname="col2"> <p>Returns uptime and current memory usage information for the Image Server, Tomcat/Platform Server, and SVGserver, or status for just the specified sever; an informational message is returned instead if the Server Supervisor is not running. </p> </td> 
  </tr> 
 </tbody> 
</table>

