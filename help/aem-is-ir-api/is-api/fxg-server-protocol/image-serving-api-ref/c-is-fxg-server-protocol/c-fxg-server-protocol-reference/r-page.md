---
title: page
description: Retrieve page. Retrieves a specific page in a multi-page FXG.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7c72ceff-30d9-4e0b-8b4f-6cb0039d389e
TQID: 'https://experienceleague.adobe.com/-YFn2qqG1ZfEQKVdQojrnYlgkCjIxvSxCJ-IKxs2gZI'
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
