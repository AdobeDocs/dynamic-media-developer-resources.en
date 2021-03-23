---
description: The following paragraph formatting commands are supported.
solution: Experience Manager
title: Paragraph formatting
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# Paragraph formatting{#paragraph-formatting}

The following paragraph formatting commands are supported.

<table id="table_5DD044E1C0614A29A2413557DF57197D"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Command </p> </th> 
   <th class="entry"> <p>Description </p> </th> 
   <th class="entry"> <p>Notes </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \pard </span> </td> 
   <td> <p>Reset paragraph formatting to default. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ql </span> </td> 
   <td> <p>Left-align text. </p> </td> 
   <td> <p>Default. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qr </span> </td> 
   <td> <p>Right-align text. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qc </span> </td> 
   <td> <p>Center text horizontally. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qj </span> </td> 
   <td> <p>Justify text horizontally. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastql </span> </td> 
   <td> <p>Left-align the last line of a paragraph. </p> </td> 
   <td> <p>Default; <span class="codeph"> textPs= </span> only; ignored if <span class="codeph"> \qj </span>is not active. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqr </span> </td> 
   <td> <p>Right-align the last line of a justified paragraph. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only; ignored if <span class="codeph"> \qj </span> is not active. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqc </span> </td> 
   <td> <p>Center the last line of a justified paragraph. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only; ignored if <span class="codeph"> \qj </span>is not active. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj </span> </td> 
   <td> <p>Sustify (stretch) the last line of a justified paragraph. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only; ignored if <span class="codeph"> \qj </span>is not active. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi <span class="varname"> N </span> </span> </td> 
   <td> <p>First line indent. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li <span class="varname"> N </span> </span> </td> 
   <td> <p>Left indent. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri <span class="varname"> N </span> </span> </td> 
   <td> <p>Right indent. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl <span class="varname"> N </span> </span> </td> 
   <td> <p>Space between lines. </p> </td> 
   <td> <p>0 (default) for automatic line spacing; positive values to only use value if larger than default line spacing; negative value to force spacing. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult <span class="varname"> N </span> </span> </td> 
   <td> <p>Line spacing multiple flag. </p> </td> 
   <td> <p>Set to 0 (default) if <span class="codeph"> \sl </span> is in twips, to 1 if <span class="codeph"> \sl </span> is in multiples of the default spacing. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb <span class="varname"> N </span> </span> </td> 
   <td> <p>Extra space before paragraph. </p> </td> 
   <td> <p>Twips; <span class="codeph"> text= </span>applies <span class="codeph"> \sb </span> to the first paragraph in the text box, <span class="codeph"> textPs= </span> does not. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa <span class="varname"> N </span> </span> </td> 
   <td> <p>Extra space after paragraph. </p> </td> 
   <td> <p>Twips; <span class="codeph"> text= </span> applies <span class="codeph"> \sa </span> to the last paragraph in the text box, <span class="codeph"> textPs= </span> does not. </p> </td> 
  </tr> 
 </tbody> 
</table>

