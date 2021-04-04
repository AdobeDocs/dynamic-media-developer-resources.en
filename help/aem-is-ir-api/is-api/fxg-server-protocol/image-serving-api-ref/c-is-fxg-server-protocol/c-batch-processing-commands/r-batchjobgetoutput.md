---
description: Retrieve the output of a submitted job.
solution: Experience Manager
title: batchjobgetoutput
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 3fb48c39-b15a-45b7-9aca-ed33f9c46c93
---
# batchjobgetoutput{#batchjobgetoutput}

Retrieve the output of a submitted job.

 This parameter:

<table id="simpletable_D8AA325968AD4FAEA7B214F0CBBF3F08"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid </span> </p> </td> 
  <td class="stentry"> <p>Job ID that was obtained at the time of submission. </p> </td> 
 </tr> 
</table>

Returns:

PDF output of the job is streamed in response; error if `jobid` is invalid or job has been deleted.

## Example {#section-0319e615fa254132a9dab59351b4c252}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobgetoutput&jobid=1005907604914d8eb63126b98f7172n76a5]
