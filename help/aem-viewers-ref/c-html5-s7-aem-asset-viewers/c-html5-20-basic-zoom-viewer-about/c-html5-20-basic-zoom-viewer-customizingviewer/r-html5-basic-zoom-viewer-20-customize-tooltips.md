---
description: On desktop systems some user interface elements like buttons have tooltips that are displayed on mouse hover.
seo-description: On desktop systems some user interface elements like buttons have tooltips that are displayed on mouse hover.
seo-title: Tooltips
solution: Experience Manager
title: Tooltips
uuid: fb32c536-800d-44fe-8fd6-8f57524729c3
feature: "Dynamic Media Classic,Viewers,SDK/API,Zoom"
role: "Developer,Business Practitioner"
---

# Tooltips{#tooltips}

On desktop systems some user interface elements like buttons have tooltips that are displayed on mouse hover.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS properties of the main viewer area**

The appearance of tooltips is controlled with the following CSS class selector:

```
.s7tooltip
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
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> Background border radius. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color </span> </p> </td> 
   <td colname="col2"> <p> Background border color. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Background color. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Text color. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Text font name. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Text font size. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>In case tooltip styles are customized from within the embedding web page, all properties have to contain `!IMPORTANT` rule. This is not necessary if tooltips are customized in the viewer's CSS file.

Example - to set up tooltips that have a grey border with 3px corner radius, black background and white text written with Arial, 11 pixels size:

```
.s7tooltip { 
 border-radius: 3px 3px 3px 3px; 
 border-color: #999999; 
 background-color: #000000; 
 color: #FFFFFF; 
 font-family: Arial, Helvetica, sans-serif; 
 font-size: 11px; 
}
```

