---
description: This document describes the material catalog for Dynamic Media Image Rendering.
solution: Experience Manager
title: Introduction
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# Introduction{#introduction}

This document describes the material catalog for Dynamic Media Image Rendering.

 **Intended audience**

This documented is intended for experienced programmers and website developers who want to leverage Dynamic Media Image Rendering for a website or a custom application.

It is assumed that the reader is familiar with Dynamic Media Image Authoring and Image Rendering, general HTTP protocol standards and conventions, and basic imaging terminology.

**Document conventions**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Literal </p> </td> 
  <td class="stentry"> <p>In syntax sections, non-italic text is literal; this does not apply to white space and the symbols [ ] { } | *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'literal' </p> </td> 
  <td class="stentry"> <p>In descriptive sections, non-italic text in single quotes is literal. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> parameter </span> </p> </td> 
  <td class="stentry"> <p>Italics indicate a variable or parameter, to be substituted with an actual value. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> attribute::Item </span> </p> </td> 
  <td class="stentry"> <p>A name prefixed with 'attribute::' refers to an image catalog attribute. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> catalog::Item </span> </td> 
  <td class="stentry"> <p>A name prefixed with 'catalog::' refers to a material catalog data field. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item </span> </p> </td> 
  <td class="stentry"> <p>A name prefixed with 'icc::' refers to a field in the ICC color profile map. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> macro::Item </span> </p> </td> 
  <td class="stentry"> <p>A name prefixed with 'macro::' refers to a field in the macro definition table. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ruleset::Item </span> </p> </td> 
  <td class="stentry"> <p>A name prefixed with 'ruleset::' refers to an element in a URL pre-processing rule set. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> default::Item </span> </p> </td> 
  <td class="stentry"> <p>A name prefixed with 'default::' refers to an attribute of the default image catalog. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> vignette::Item </span> </p> </td> 
  <td class="stentry"> <p>A name prefixed with 'vignette::' refers to a field in the vignette map. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname"> optional </span> ] </p> </td> 
  <td class="stentry"> <p>Optional syntax elements are enclosed by square brackets. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname"> optional </span> ] </p> </td> 
  <td class="stentry"> <p>The optional syntax element may be repeated none or more times. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item1 </span>| <span class="varname"> item2 </span> </p> </td> 
  <td class="stentry"> <p>A vertical bar indicates that either the single syntax item to the left or the item to right may be used. Exactly one item must be selected. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>{ <span class="varname"> group </span> } </p> </td> 
  <td class="stentry"> <p>Curly braces are used to group syntax elements. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*{ <span class="varname"> group </span> } </p> </td> 
  <td class="stentry"> <p>The syntax elements within the group may be repeated one or more times. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>White space. </p> </td> 
  <td class="stentry"> <p>White space (spaces or tabs) is not allowed in HTTP requests. This document occasionally uses white space between syntactic elements for clarity only. </p> </td> 
 </tr> 
</table>

