---
description: The extensible metadata platform keywords of an asset.
solution: Experience Manager
title: XmpKeywords
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f1ad16c8-cba2-4ef0-9558-6a4086c71393
---
# [!DNL XmpKeywords]{#xmpkeywords}

The extensible metadata platform keywords of an asset.

 Syntax 

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> items</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>A comma-separated list of keywords that get merged into the <span class="codeph"> dc:subject=</span> XMP property node. If a comma appears in any of the individual values, it needs to be escaped by a backslash (\) character. A literal backslash is the usual double-backslash (\\). </p> </td> 
  </tr> 
 </tbody> 
</table>
