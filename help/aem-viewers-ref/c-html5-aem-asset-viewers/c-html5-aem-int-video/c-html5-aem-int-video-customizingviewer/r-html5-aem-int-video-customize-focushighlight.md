---
description: Input focus highlight displayed around focused viewer user interface element is controlled with the CSS class selector.
seo-description: Input focus highlight displayed around focused viewer user interface element is controlled with the CSS class selector.
seo-title: Focus highlight
solution: Experience Manager
title: Focus highlight
topic: Dynamic Media
uuid: 44057e10-98b6-4316-bf6c-9bf569be6a50
---

# Focus highlight{#focus-highlight}

Input focus highlight displayed around focused viewer user interface element is controlled with the CSS class selector.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS properties**

The appearance is controlled with the following CSS class selector:

```
.s7interactivevideoviewer *:focus
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS property </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> outline </span> </p> </td> 
   <td colname="col2"> <p>Focus highlight style. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to disable the default browser focus highlight for all viewer user interface elements, add the following CSS selector to viewer's style sheet:

```
.s7interactivevideoviewer *:focus { 
 outline: none; 
}
```

