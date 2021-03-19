---
description: Standard alerts are sent with a consolidated email message at the end of the configured averaging interval.
seo-description: Standard alerts are sent with a consolidated email message at the end of the configured averaging interval.
seo-title: Standard alerts
solution: Experience Manager
title: Standard alerts
uuid: d3294434-a44b-4742-9d77-a6945760d33c
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
---

# Standard alerts{#standard-alerts}

Standard alerts are sent with a consolidated email message at the end of the configured averaging interval.

The following table describes each type of standard alert.

<table id="table_02611F1B920E48A6973BFA969CA564EB"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Alert Type</b> </th> 
   <th class="entry"> <b>Title Id</b> </th> 
   <th class="entry"> <b>Description</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>Locked Request </p> </td> 
   <td> <p>Lock </p> </td> 
   <td> <p>Sent when a request fails to return a response to the client within the specified threshold. Can be indicative of hung requests, which can cause depletion of the Java thread pool. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>High Concurrency </p> </td> 
   <td> <p>Conc </p> </td> 
   <td> Emitted when the number of requests that are processed concurrently (the <i>overlap</i>) exceeds the specified threshold. Can be indicative of a server overload condition. </td> 
  </tr> 
  <tr> 
   <td> <p>Minimum Traffic </p> </td> 
   <td> <p>Traf </p> </td> 
   <td> <p>Generated when the overall request rate falls below the specified threshold. Typically indicates a server communication issue (e.g. when a server is taken off line). </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Error Rate </p> </td> 
   <td> <p>Error </p> </td> 
   <td> <p>Emitted when the average rate of HTTP error responses during the sampling interval exceeds the specified threshold. Can be indicative of configuration issues, missing images, or website programming or database errors. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Response Time </p> </td> 
   <td> <p>RTime </p> </td> 
   <td> <p>Sent when the average request processing time during the sampling interval grows above the specified threshold. Typically indicates a temporary or persistent overload condition of the server or backend image storage system. </p> <p>Error responses are not considered when calculating the average response time. </p> </td> 
  </tr> 
 </tbody> 
</table>

