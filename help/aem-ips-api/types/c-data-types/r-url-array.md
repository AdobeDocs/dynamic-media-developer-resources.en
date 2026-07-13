---
description: An array of URLS for invalidating CDN cache.
solution: Experience Manager
title: UrlArray
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 61225fb2-7c25-4f9c-82c9-02bf69995028
TQID: 'https://experienceleague.adobe.com/6NRN2CnA3hA3Y5GOgrpc4ok4RyIf4XftMr5EeuGwDr8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# [!DNL UrlArray]{#urlarray}

An array of URLS for invalidating CDN cache.

 **Supported Since**

4.5.0, patch 2011-02

## Parameters {#section-20f617c881f34dc287989cbb20ee494d}

<table id="table_A28FC686DFB84198BF6671F953E8F044"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Name</b> </th> 
   <th class="entry"> <b> Type</b> </th> 
   <th class="entry"> <b> Description</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> items</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td> <p> The list of URLs to invalidate. Limited to maximum of 1000 URLs by the WSDL definition. </p> </td> 
  </tr> 
 </tbody> 
</table>

