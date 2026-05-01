---
title: Focus highlight
description: Input focus highlight displayed around focused viewer user interface element is controlled with the CSS class selector.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 05ac1a70-c20d-4ddf-942c-181f101cb1d8
TQID: https://experienceleague.adobe.com/eKerD4LK8gcx7bEkZ6-xdrVFREoqhLkDsu1ik2ICCZg
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# Focus highlight{#focus-highlight}

Input focus highlight displayed around focused viewer user interface element is controlled with the CSS class selector.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS properties**

The appearance is controlled with the following CSS class selector:

```
.s7video360viewer *:focus
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
.s7video360viewer *:focus { 
 outline: none; 
}
```
