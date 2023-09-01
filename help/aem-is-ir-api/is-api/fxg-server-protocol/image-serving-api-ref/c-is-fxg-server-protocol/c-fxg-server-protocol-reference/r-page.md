---
title: page
description: Retrieve page. Retrieves a specific page in a multi-page FXG.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7c72ceff-30d9-4e0b-8b4f-6cb0039d389e
---
# page{#page}

Retrieve page. Retrieves a specific page in a multi-page FXG.

 `page= *`val`*`

<table id="simpletable_E92560F812B64A36A3D108CA7DEED5AC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Page number (first page is 1). </p></td> 
 </tr> 
</table>

## Default {#section-3fd7fcc525b947c7a95457e50414ac9e}

If `page` is not specified, then the first page is returned for raster output and all pages for PDF output.
