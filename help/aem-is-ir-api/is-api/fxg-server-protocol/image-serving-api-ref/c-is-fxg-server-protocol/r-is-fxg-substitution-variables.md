---
description: Substitution variable are used to transfer values from the request URL to FXG templates stored on the server.
solution: Experience Manager
title: Substitution Variables
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 539d8863-e94d-45dc-bb8c-3db7bead0051
TQID: https://experienceleague.adobe.com/Ck-HwD4vFVUskVCh8LfreLTGyGLOplUbZLFcdzBw8V8
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
# Substitution Variables{#substitution-variables}

Substitution variable are used to transfer values from the request URL to FXG templates stored on the server.

 ` $ *`var`*= *`value`*`

<table id="simpletable_76B381800C0D411F87CD551FC30B0579"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>Variable name. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
  <td class="stentry"> <p>Value to which the variable is to be set (string). </p> </td> 
 </tr> 
</table>

* Variable definitions and references may occur in the query portion of the request URL. 
* Variables are defined as above, similar to other IS commands; the leading '$' identifies the command as a variable definition. 
* The variable name `*`var`*` is case-sensitive and may consist of any combination of letters, numbers, '-', and '_'. 
* Important value must be single-pass URL-encoded for safe HTTP transmission.
