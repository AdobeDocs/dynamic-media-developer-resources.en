---
description: Within this type, the pageReset field is meaningful for RenderSet and Catalog image asset types 


solution: Experience Manager
title: ImageSetMemberUpdate

feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Administrator
---

# ImageSetMemberUpdate{#imagesetmemberupdate}

Within this type, the pageReset field is meaningful for RenderSet and Catalog image asset types:

* For `RenderSet`, `pageReset` indicates the start of a new render view/swatch group. 

* For Catalog, `pageReset` indicates the start of a new page view. Typically, there are 2 page images per page view, but you can have more or fewer.

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Asset handle in the image set member array. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pageReset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">Resets the page. <p>Setting is ignored and value is forced to true for <span class="codeph"> ImageSet</span> and <span class="codeph"> SpinSet</span>. </p></td> 
  </tr> 
 </tbody> 
</table>

