---
title: Image Serving components
description: Dynamic Media Image Serving consists of the following components. 
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67dd37f3-b11e-42d6-b308-7c1e76a8f2a9
---
# Image Serving components{#image-serving-components}

Dynamic Media Image Serving consists of the following components:

<table id="table_534AF33FE5C4453EACAE0DF35E8E3B63"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Component </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Server Supervisor </p> </td> 
   <td colname="col2"> <p>A stand-alone executable responsible for starting, stopping, and ensuring the health of the other components. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>It provides the environment for most Java-based components. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Monitoring/Alerting Service </p> </td> 
   <td colname="col2"> <p>J2EE application. Provides server monitoring and email alerting. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>[!DNL Platform Server] </p> </td> 
   <td colname="col2"> <p>J2EE application. Manages client connections, logging, communications with other components. HTTP access at <span class="filepath"> /is/image</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Caching Service </p> </td> 
   <td colname="col2"> <p>J2EE application. Manages the [!DNL Platform Server]'s data caches. HTTP access at /is/cache. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Image Server </p> </td> 
   <td colname="col2"> <p>It performs all image-processing and image file I/O operations. Both 32-bit and 64-bit executables are available for Linux&reg; (32 bit only for Windows). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ATE Text Render Component </p> </td> 
   <td colname="col2"> <p>One or more instances of the text rendering service may be active when <span class="codeph"> textPs=</span> operations are run. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SVG Render Component </p> </td> 
   <td colname="col2"> <p>Stand-alone Java&trade; application (not hosted by Tomcat). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dynamic Media Image Rendering (aka. Render Server) </p> </td> 
   <td colname="col2"> <p>It requires a separate license to activate. HTTP access at <span class="filepath"> /ir/render</span>. All Image Rendering functionality is integrated into the [!DNL Platform Server] and the Image Server, with no separate executable components. </p> </td> 
  </tr> 
 </tbody> 
</table>

Additional configuration settings are provided by the default catalog ( [!DNL default.ini]) or specific image catalogs (see [Image Catalogs](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) for details).
