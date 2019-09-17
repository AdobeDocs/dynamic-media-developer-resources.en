---
description: Delete the output of a job.
seo-description: Delete the output of a job.
seo-title: batchjobdelete
solution: Experience Manager
title: batchjobdelete
topic: Scene7 Image Serving - Image Rendering API
uuid: d19ed1c8-e13b-4da4-90e3-6bb0dcce2a12
---

# batchjobdelete{#batchjobdelete}

Delete the output of a job.

 If a job is running currently, it is stopped immediately and all its processing info is deleted. If the job had completed successfully, its output file is deleted.

This parameter:

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> jobid</span> </p> </td> 
  <td class="stentry"> <p>Job ID that was obtained at the time of submission. </p></td> 
 </tr> 
</table>

Returns:

Status of job at the time the deletion request was received, error if `jobid` is invalid or job had already been deleted.

## Example {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5] 
