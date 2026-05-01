---
description: Client message. Provides a mechanism for clients to insert short text messages into the server log.
solution: Experience Manager
title: message
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 47e51181-714c-4b25-a375-f3b2238cd534
TQID: https://experienceleague.adobe.com/n0dsZzQc4V7f38nDN2SuF461VuEyF02X86glR-Dgu1o
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
# message{#message}

Client message. Provides a mechanism for clients to insert short text messages into the server log.

 `req=message&message= *`string`*`

<table id="simpletable_9AF29AA336C4447BBC2FD4A7D43ED91B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> string</span> </p> </td> 
  <td class="stentry"> <p>Message string. </p></td> 
 </tr> 
</table>

The HTTP response is not cacheable. An empty response is returned with MIME type `text/plain`.
