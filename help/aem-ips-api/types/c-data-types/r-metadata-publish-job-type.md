---
description: Publishes metadata to the metadata server.


solution: Experience Manager
title: MetadataPublishJobType

feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Administrator
---

# MetadataPublishJobType{#metadatapublishjobtype}

Publishes metadata to the metadata server.

 Syntax 

## Parameters {#section-6c51fa689b3648fbb7c7945a7e176d0a}

<table id="table_23B5CFC5C3F946F9AFDB6A83A1AAB7AF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> forcePublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">Set to <span class="codeph"> True</span> to publish <i>all</i> data to the metadata server again. <p>Note:  Depending on the amount of data, this can take several minutes to a few hours. </p><p>Do not set this parameter if you want to publish new or changed metadata only. </p></td> 
  </tr> 
 </tbody> 
</table>

