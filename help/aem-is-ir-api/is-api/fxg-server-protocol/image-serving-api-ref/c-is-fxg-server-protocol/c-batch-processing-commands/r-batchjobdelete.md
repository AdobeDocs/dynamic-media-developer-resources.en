---
title: batchjobdelete
description: Delete the output of a job.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9aca6693-32ac-4abd-9595-95bce60050ec
TQID: https://experienceleague.adobe.com/F-CmGkJK4OMJfBiPD3SiqI2oXnX2j9fIK0lw-R5HXFM
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
# batchjobdelete{#batchjobdelete}

Delete the output of a job.

 If a job is running currently, it is stopped immediately, and all its processing info is deleted. If the job had completed successfully, its output file is deleted.

This parameter:

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> job_id</span> </p> </td> 
  <td class="stentry"> <p>Job ID that was obtained at the time of submission. </p></td> 
 </tr> 
</table>

Returns:

Status of job at the time the deletion request was received, error if `jobid` is invalid or job had already been deleted.

## Example {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5`
