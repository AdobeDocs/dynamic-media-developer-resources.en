---
description: Retrieve the output of a submitted job.
seo-description: Retrieve the output of a submitted job.
seo-title: batchjobgetoutput
solution: Experience Manager
title: batchjobgetoutput
topic: Dynamic Media Image Serving - Image Rendering API
uuid: c2d49cc2-3223-4f0f-8ba7-4f74a5f76789
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
