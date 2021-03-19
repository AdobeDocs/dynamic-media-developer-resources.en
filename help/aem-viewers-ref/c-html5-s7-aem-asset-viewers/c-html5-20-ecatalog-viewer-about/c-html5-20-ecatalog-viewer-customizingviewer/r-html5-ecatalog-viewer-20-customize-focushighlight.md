---
description: Input focus highlight displayed around the focused viewer user interface element.
seo-description: Input focus highlight displayed around the focused viewer user interface element.
seo-title: Focus highlight
solution: Experience Manager
title: Focus highlight
uuid: 50411b68-8d01-4240-b548-a6c51374a8c6
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
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

Example - to disable the default browser focus highlight for all viewer user interface elements add the following CSS selector to the viewer's style sheet:

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```

