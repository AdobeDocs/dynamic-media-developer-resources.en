---
title: batchjobbriefstatus
description: Retrieve summarized status of a submitted job.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b31bdbb-3c2c-4f7f-ba95-d3e710270be0
TQID: https://experienceleague.adobe.com/oZhQiue9cUUTXGfboPl--U7-5cOr--Sw3lEdVqO9F0c
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
# batchjobbriefstatus{#batchjobbriefstatus}

Retrieve summarized status of a submitted job.

This parameter:

<table id="simpletable_86E581DBB352479CB4CB531434D91E83"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid </span> </p> </td> 
  <td class="stentry"> <p>Job ID that was obtained at the time of submission. </p> </td> 
 </tr> 
</table>

Returns:

Brief status of job in XML format; error if jobid is invalid or job has been deleted.

## Example {#section-806460949bb043438ad4dd4e7ab74145}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobbriefstatus&jobid=1005907604914d8eb63126b98f7172n76a5]
