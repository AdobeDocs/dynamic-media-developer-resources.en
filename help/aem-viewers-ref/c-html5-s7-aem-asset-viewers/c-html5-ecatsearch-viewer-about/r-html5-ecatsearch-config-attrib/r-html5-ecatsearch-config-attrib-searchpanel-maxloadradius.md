---
description: SearchPanel.maxloadradius
solution: Experience Manager
title: SearchPanel.maxloadradius
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: c2bbcb99-eeef-4793-a132-d0bd1fefb534
TQID: 'https://experienceleague.adobe.com/h1vgh-2w1mYZXx7MR7korb48n9JuS-pMPFk3HIt4928'
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
# SearchPanel.maxloadradius{#searchpanel-maxloadradius}

 [!DNL `[SearchPanel.|<containerId>_searchPanel.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>Specifies the component preload behavior. </p> <p>When set to <span class="codeph"> -1</span> all thumbnails are loaded simultaneously when the component is initialized or the asset changes. </p> <p> When set to <span class="codeph"> 0</span> only visible thumbnails are loaded. </p> <p>Set <span class="codeph"><span class="varname"> preloadnbr</span></span> to define how many invisible rows around the visible area are preloaded. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-4b7952997f9240e581d21bcdb173f9af}

Optional.

## Default {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

[!DNL `1`]

## Example {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

[!DNL `maxloadradius=0`]

