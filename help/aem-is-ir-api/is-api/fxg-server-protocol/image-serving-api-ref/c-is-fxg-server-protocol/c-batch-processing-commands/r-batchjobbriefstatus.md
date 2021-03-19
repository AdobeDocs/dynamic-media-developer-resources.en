---
description: Retrieve summarized status of a submitted job.
seo-description: Retrieve summarized status of a submitted job.
seo-title: batchjobbriefstatus
solution: Experience Manager
title: batchjobbriefstatus
uuid: 601e8395-8a77-4324-9cd7-5fe321bc91e3
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Business Practitioner"
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
