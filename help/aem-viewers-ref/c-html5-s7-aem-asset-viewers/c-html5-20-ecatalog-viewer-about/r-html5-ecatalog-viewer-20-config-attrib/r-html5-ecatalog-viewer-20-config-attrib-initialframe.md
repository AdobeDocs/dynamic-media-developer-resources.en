---
title: InitialFrame
description: InitialFrame
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 28b6b981-94f6-4136-b322-992e18d154db
TQID: https://experienceleague.adobe.com/I4AblgiasZr--R5-zhUHHcgYg4llGy5l1n5kWhQq5aU
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# InitialFrame{#initialframe}

 ` initialFrame= *`frame`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> frame</span></span> </p> </td> 
   <td colname="col2"> <p> Specifies a zero-based spread index to display on viewer load. The index matches the index of the spread in landscape mode. If the viewer is rotated to portrait, the viewer displays the leftmost page from the spread that is pointed to by <span class="codeph"> frameIdx</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-fc7c012c91d1419b8a5bb60d28e17327}

Optional.

## Default {#section-bbc6ebad3af54fd79837515c270e6ddf}

`0`

## Example {#section-cbc6684eb22e4d0883edc4b3d5742336}

When specified in the viewer URL. 

```
initialFrame=2
```
