---
description: Use the following commands for encoding characters.
seo-description: Use the following commands for encoding characters.
seo-title: Character encoding
solution: Experience Manager
title: Character encoding
uuid: 7b19b831-b40c-4f26-83a4-732c578dbbf0
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
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
   <td> <p><span class="varname"> HH</span> must be a 2 digit hex value. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\u<span class="varname"> N</span></span> </td> 
   <td> <p>Single Unicode character. </p> </td> 
   <td> <p><span class="varname"> N</span> is a signed 2 byte integer and thus a Unicode value greater than 32767 must be expressed as a negative number. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\uc<span class="varname"> N</span></span> </td> 
   <td> <p>Unicode character size. </p> </td> 
   <td> <p>Number of bytes corresponding to given Unicode character. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch </span> </td> 
   <td> <p>Characters from low-ANSI area follow. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \hich </span> </td> 
   <td> <p>Characters from high-ANSI area follow. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch </span> </td> 
   <td> <p>Double-byte characters follow. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

