---
description: Submit a new batch job.
solution: Experience Manager
title: batchjobsubmit
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4ab2f6e4-cd68-4f1e-ab54-6f5e9bfc87cb
---
# batchjobsubmit{#batchjobsubmit}

Submit a new batch job.

This parameter:

<table id="simpletable_11A94D630A21426F9A1CEF5EB3B9E789"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobdata </span> </p> </td> 
  <td class="stentry"> <p>XML snippet of complete job data. </p> </td> 
 </tr> 
</table>

Returns:

<table id="simpletable_7C82E4A8520440F5A5ABBC1BCB286AB2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Status of job </p> </td> 
  <td class="stentry"> <p>Whether submission succeeded or failed; if succeeded, job ID in XML format. </p> </td> 
 </tr> 
</table>

## Example {#section-3886e8352e26419c97b24df21ca7f6fd}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobsubmit&jobdata=<URLEncodedXMLFileContents>`
