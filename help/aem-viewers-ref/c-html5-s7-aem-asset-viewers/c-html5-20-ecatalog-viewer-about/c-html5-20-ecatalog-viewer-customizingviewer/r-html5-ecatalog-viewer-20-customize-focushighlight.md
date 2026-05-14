---
title: Focus highlight
description: Input focus highlight displayed around the focused viewer user interface element.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3d5737d7-1295-46a9-9b84-c43269e5a914
TQID: 'https://experienceleague.adobe.com/8xcQUHsvWwaKyz9-UA1cQbFhQmOpfiXGJ4EpERAJJow'
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
# Focus highlight{#focus-highlight}

Input focus highlight displayed around the focused viewer user interface element.

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

The appearance of the focus highlight is controlled with the following CSS class selector:

```
.s7ecatalogviewer *:focus
```

**CSS properties of the focus highlight**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> outline </span> </p> </td> 
   <td colname="col2"> <p> Focus highlight style. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - To disable the default browser focus highlight for all viewer user interface elements add the following CSS selector to the viewer's style sheet:

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```
