---
description: Use the following commands for basic character formatting.
solution: Experience Manager
title: Basic character formatting
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: d3bd6d4d-d7bd-4c9b-bc9e-7edaaac6378e
---
# Basic character formatting{#basic-character-formatting}

Use the following commands for basic character formatting.

<table id="table_65415B84652F4E7497299AD90AE7C191"> 
 <thead> 
  <tr> 
   <th class="entry"> Command </th> 
   <th class="entry"> Description </th> 
   <th class="entry"> Notes </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \plain </span> </td> 
   <td> <p>Reset character formatting to default. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \f <span class="varname"> N </span> </span> </td> 
   <td> <p>Font face. </p> </td> 
   <td> <p> <span class="codeph"> \fonttbl </span> index. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fs <span class="varname"> N </span> </span> </td> 
   <td> <p>Font size. </p> </td> 
   <td> <p>Half-points; default is 24. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cf <span class="varname"> N </span> </span> </td> 
   <td> <p>Font color. </p> </td> 
   <td> <p>0-based index into color table. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \b </span> </td> 
   <td> <p>Bold style. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \i </span> </td> 
   <td> <p>Italic style. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sub </span> </td> 
   <td> <p>Subscript. </p> </td> 
   <td> <p>Reduces font size. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \super </span> </td> 
   <td> <p>Superscript. </p> </td> 
   <td> <p>Reduces font size. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <span class="codeph"> \ul </span> </td> 
   <td> <p>Underline. </p> </td> 
   <td> <p>Image Serving also recognizes the following RTF underlining commands: </p> <p> 
     <ul id="ul_EF2077DD51F94E2E94D8F1FA661F95DE"> 
      <li id="li_F9382148CCCC4A6AB373DD96D28B71EE"> <span class="codeph"> \uld </span> </li> 
      <li id="li_141276B2082E4AD0A8C7D3BDDADD6EE2"> <span class="codeph"> \uldash </span> </li> 
      <li id="li_32CE2C69EEFE462FB21F49FF52A65B0B"> <span class="codeph"> \uldashd </span> </li> 
      <li id="li_DCF3CD4F884845A5A6B84BDD8DB3A572"> <span class="codeph"> \uldashdd </span> </li> 
      <li id="li_FDEF96CCE14D41BDB878AADCFF73068F"> <span class="codeph"> \uldb </span> </li> 
      <li id="li_482CCC6F5D8544CCA69DF2A070097ABD"> <span class="codeph"> \ulth </span> </li> 
      <li id="li_F11C79A6640B4C0684CA5D9733E49F43"> <span class="codeph"> \ulw </span> </li> 
      <li id="li_84F94D17372B4C0494A9F8AEC951C556"> <span class="codeph"> \ulwave </span> </li> 
     </ul> </p> <p>These are implemented at this time as a standard <span class="codeph"> \ul </span> underlining. All other RTF underlining commands are ignored. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ulnone </span> </td> 
   <td> <p>turn off underlining </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ul0 </span> </td> 
   <td> <p>turn off underlining </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \caps </span> </td> 
   <td> <p>uppercase </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \scaps </span> </td> 
   <td> <p>lowercase ("small caps") </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only. </p> </td> 
  </tr> 
 </tbody> 
</table>
