---
description: The following document properties are supported in text boxes.
seo-description: The following document properties are supported in text boxes.
seo-title: Document (text box) properties
solution: Experience Manager
title: Document (text box) properties
uuid: 743a773a-83b0-4667-9c67-4cefbfe77bbd
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# Document (text box) properties{#document-text-box-properties}

The following document properties are supported in text boxes.

<table id="table_8E1DF8E6BD894D7A9ACFC839918E2315"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Command</b> </th> 
   <th class="entry"> <b>Description</b> </th> 
   <th class="entry"> <b>Notes</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \fonttbl </span> </td> 
   <td> <p>Font table. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fcharset <span class="varname"> N </span> </span> </td> 
   <td> <p>Character set for font <i>N</i>. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \colortbl </span> </td> 
   <td> <p>RGB color table. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cmykcolortbl </span> </td> 
   <td> <p>CMYK color table. </p> </td> 
   <td> <p>Dynamic Media extension. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \*\iscolortbl </span> </td> 
   <td> <p>Color table for Image Serving colors. </p> </td> 
   <td> <p>Dynamic Media extension; <span class="codeph"> textPs= </span> only </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \red <span class="varname"> N </span> </span> </td> 
   <td> <p>Red color component. </p> </td> 
   <td> <p>May only appear in <span class="codeph"> \colortbl </span>; 0…255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \green <span class="varname"> N </span> </span> </td> 
   <td> <p>Green color component. </p> </td> 
   <td> <p>May only appear in <span class="codeph"> \colortbl </span>; 0…255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \blue <span class="varname"> N </span> </span> </td> 
   <td> <p>Blue color component. </p> </td> 
   <td> <p>May only appear in <span class="codeph"> \colortbl </span>; 0…255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cyan <span class="varname"> N </span> </span> </td> 
   <td> <p>Cyan color component. </p> </td> 
   <td> <p>Dynamic Media extension; may only appear in <span class="codeph"> \cmykcolortbl </span>; 0…100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \magenta <span class="varname"> N </span> </span> </td> 
   <td> <p>Magenta color component. </p> </td> 
   <td> <p>Dynamic Media extension; may only appear in <span class="codeph"> \cmykcolortbl </span>; 0…100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \yellow <span class="varname"> N </span> </span> </td> 
   <td> <p>Yellow color component. </p> </td> 
   <td> <p>Dynamic Media extension; may only appear in <span class="codeph"> \cmykcolortbl </span>; 0…100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \black <span class="varname"> N </span> </span> </td> 
   <td> <p>Black color component. </p> </td> 
   <td> <p>Dynamic Media extension; may only appear in <span class="codeph"> \cmykcolortbl </span>; 0…100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margl <span class="varname"> N </span> </span> </td> 
   <td> <p>Left margin. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> only </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margr <span class="varname"> N </span> </span> </td> 
   <td> <p>Right margin. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> only </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margt <span class="varname"> N </span> </span> </td> 
   <td> <p>Top margin. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> only </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margb <span class="varname"> N </span> </span> </td> 
   <td> <p>Bottom margin. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> only </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalt </span> </td> 
   <td> <p>Top-align text in text box. </p> </td> 
   <td> <p>Default </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalb </span> </td> 
   <td> <p>Bottom-align text in text box. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalc </span> </td> 
   <td> <p>Center text in text box. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \stextflow <span class="varname"> N </span> </span> </td> 
   <td> <p>Text flow orientation. </p> </td> 
   <td> <p>Language-specific text flow; <span class="codeph"> textPs= </span> only 0 (default) left-right, top-bottom (European) 1 top-bottom, right-left (Far Eastern) </p> </td> 
  </tr> 
 </tbody> 
</table>

