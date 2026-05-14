---
title: direction
description: direction
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 0f78a835-9057-4c79-843a-52b33a1bdd3f
TQID: 'https://experienceleague.adobe.com/tNKu0P8Sgoxas-opiWd1GWkuWYWDfXE0-j1A-p-j-jM'
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
# direction{#direction}

 [!DNL `direction=auto|left|right`]

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p>Specifies the way pages are displayed in the main view and thumbnails. It also specifies the way that the user interacts with the viewer user interface to change between catalog frames. </p> <p>When <span class="codeph"> left </span> is used it sets a right alignment for the initial page, and a left alignment for the last page. It stitches individual page subimages for left-to-right rendering order. It also sets the main view to use right-to-left slide animation to advance the catalog (in case <span class="codeph"> PageView.frametransition </span> is set to slide). Finally, thumbnails are set for a left-to-right fill order. </p> <p>Similarly, when <span class="codeph"> right </span> is used it sets a left alignment for the initial page, and a right alignment for the last page. It stitches individual page subimages for right-to-left rendering order. It also sets the main view to use left-to-right slide animation to advance the catalog (in case <span class="codeph"> PageView.frametransition </span> is set to slide). Finally, it reverses the thumbnails order so that the thumbnails view is filled in right-to-left, top-to-bottom direction. </p> <p>When <span class="codeph"> auto </span> is set, the viewer applies <span class="codeph"> right </span> mode when locale is set to <span class="codeph"> ja; </span>otherwise, it uses <span class="codeph"> left </span> mode. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-a66ce10d6c0b449883f654e7e0657e2c}

Optional.

## Default {#section-2879062cee1d4030b43ba3b19693f4f8}

[!DNL `auto`]

## Example {#section-798e4fc8dd9b4b059171b41a608a96ce}

[!DNL `direction=right`]
