---
description: Use the following commands for advanced text formatting.
seo-description: Use the following commands for advanced text formatting.
seo-title: Advanced text formatting
solution: Experience Manager
title: Advanced text formatting
topic: Scene7 Image Serving - Image Rendering API
uuid: 340166a5-5aef-4081-9114-a715cde68891
---

# Advanced text formatting{#advanced-text-formatting}

Use the following commands for advanced text formatting.

<table id="table_43B2EB887C0F471BB60C23B570E7D3D2"> 
 <thead> 
  <tr> 
   <th class="entry"> Command </th> 
   <th class="entry"> Description </th> 
   <th class="entry"> Notes </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \dn <span class="varname"> N </span> </span> </td> 
   <td> <p>Subscript without font size change. </p> </td> 
   <td> <p>Position in half-points; default is 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up <span class="varname"> N </span> </span> </td> 
   <td> <p>Superscript without font size change. </p> </td> 
   <td> <p>Position in half-points; default is 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerning <span class="varname"> N </span> </span> </td> 
   <td> <p>Disable/enable at specified font size. </p> </td> 
   <td> <p>Font size in half-points, above which to apply kerning; 0 to disable kerning; default is 1 for kerning all font sizes over ½ point. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningoptical </span> </td> 
   <td> <p>Select optical kerning. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningmetric </span> </td> 
   <td> <p>Select metric kerning. </p> </td> 
   <td> <p>Default. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expnd <span class="varname"> N </span> </span> </td> 
   <td> <p>Modify character spacing. </p> </td> 
   <td> <p>Positive or negative quarter-points; default is 0. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expndtw <span class="varname"> N </span> </span> </td> 
   <td> <p>Modify character spacing. </p> </td> 
   <td> <p>Positive or negative twips. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex <span class="varname"> N </span> </span> </td> 
   <td> <p>Horizontal character scaling. </p> </td> 
   <td> <p>Positive or negative percent; default is 100. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley <span class="varname"> N </span> </span> </td> 
   <td> <p>Vertical character scaling. </p> </td> 
   <td> <p>Positive or negative percent; default is 100; Scene7 extension. </p> <p> <span class="codeph"> \charscaley </span> also scales line spacing when applied with <span class="codeph"> text= </span>. <span class="codeph"> textPs= </span> always preserves line spacing regardless of the amount of vertical character scaling. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch </span> </td> 
   <td> <p>Select left-to-right character flow. </p> </td> 
   <td> <p>Default. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch </span> </td> 
   <td> <p>Select right-to-left character flow. </p> </td> 
   <td> <p> <span class="codeph"> text= </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfit <span class="varname"> N </span> </span> </td> 
   <td> <p>Enable copy-fitting and set largest allowed font size. </p> </td> 
   <td> <p>Font size in half-points; <span class="codeph"> textPs= </span> only; Scene7 extension. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines <span class="varname"> N </span> </span> </td> 
   <td> <p>Maximum copy-fit lines (soft limiting). </p> </td> 
   <td> <p>0 for no line limitation; <span class="codeph"> textPs= </span> only; Scene7 extension. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines <span class="varname"> N </span> </span> </td> 
   <td> <p>Maximum copy-fit lines (truncating). </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only; Scene7 extension. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir <span class="varname"> N </span> </span> </td> 
   <td> <p>Character orientation. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only; ignored for non-Roman fonts; ignored when <span class="codeph"> \stextflow1 </span> is not in effect. </p> <p>0 vertical (default). </p> <p>1 rotated 90 degrees clockwise. </p> </td> 
  </tr> 
 </tbody> 
</table>

