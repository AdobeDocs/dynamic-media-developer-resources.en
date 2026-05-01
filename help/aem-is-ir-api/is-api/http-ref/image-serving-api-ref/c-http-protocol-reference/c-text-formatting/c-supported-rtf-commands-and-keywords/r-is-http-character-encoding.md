---
title: Character encoding
description: Use the following commands for encoding characters.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a03f08f7-e9cc-458f-9ff0-7721f1dbc4cc
TQID: https://experienceleague.adobe.com/iYe2o4wgRTU7XROIkQlD-1dygZnw-xGSCkMAkESuIa0
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
# Character encoding{#character-encoding}

Use the following commands for encoding characters.

<table id="table_EB0C1B674BEA4A37964FB4BF559E0005"> 
 <thead> 
  <tr> 
   <th class="entry"> Command </th> 
   <th class="entry"> Description </th> 
   <th class="entry"> Notes </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph">\'<span class="varname"> HH</span></span> </td> 
   <td> <p>Single 8-bit character. </p> </td> 
   <td> <p><span class="varname"> HH</span> must be a 2-digit hex value. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\u<span class="varname"> N</span></span> </td> 
   <td> <p>Single Unicode character. </p> </td> 
   <td> <p><span class="varname"> N</span> is a signed 2-byte integer and thus a Unicode value greater than 32767 must be expressed as a negative number. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\uc<span class="varname"> N</span></span> </td> 
   <td> <p>Unicode character size. </p> </td> 
   <td> <p>Number of bytes corresponding to a given Unicode character. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch </span> </td> 
   <td> <p>Characters from the low-ANSI area. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \hich </span> </td> 
   <td> <p>Characters from the high-ANSI area. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch </span> </td> 
   <td> <p>Double-byte characters follow. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>
