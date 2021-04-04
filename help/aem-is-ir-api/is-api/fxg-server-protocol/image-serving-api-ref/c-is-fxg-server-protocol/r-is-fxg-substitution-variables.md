---
description: Substitution variable are used to transfer values from the request URL to FXG templates stored on the server.
solution: Experience Manager
title: Substitution Variables
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 539d8863-e94d-45dc-bb8c-3db7bead0051
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
