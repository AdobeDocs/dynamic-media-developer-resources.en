---
description: Retrieve detailed status of a submitted job.
seo-description: Retrieve detailed status of a submitted job.
seo-title: batchjobdetailedstatus
solution: Experience Manager
title: batchjobdetailedstatus
topic: Dynamic Media Image Serving - Image Rendering API
uuid: a79302ce-745b-44d8-9cb6-ed8d37530197
---

# batchjobdetailedstatus{#batchjobdetailedstatus}

Retrieve detailed status of a submitted job.

This parameter:

<table id="simpletable_9C379451927C4058834640377C0BD7A0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid </span> </p> </td> 
  <td class="stentry"> <p>Job ID that was obtained at the time of submission. </p> </td> 
 </tr> 
</table>

Returns:

Detailed status of job in XML format; error if `jobid` is invalid or job has been deleted.

## Example {#section-55f463750afe4814b5fdbaa2f1aafab4}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdetailedstatus&jobid=1005907604914d8eb63126b98f7172n76a5` 
