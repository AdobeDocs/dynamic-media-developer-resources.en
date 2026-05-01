---
description: Publishes metadata to the metadata server.
solution: Experience Manager
title: MetadataPublishJobType
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: b90d27c0-9398-4597-bcce-3c36a371df22
TQID: https://experienceleague.adobe.com/4DwQSdUcq8c0VzPZgL1XzQGlkBKidZoKgNzN-dnTDNY
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
---
# [!DNL MetadataPublishJobType]{#metadatapublishjobtype}

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
