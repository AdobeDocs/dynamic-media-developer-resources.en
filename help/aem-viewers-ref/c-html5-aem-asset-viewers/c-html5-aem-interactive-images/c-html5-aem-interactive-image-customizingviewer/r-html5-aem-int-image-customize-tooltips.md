---
description: On desktop systems some user interface elements like buttons have tool tips that are displayed on mouse hover.
seo-description: On desktop systems some user interface elements like buttons have tool tips that are displayed on mouse hover.
seo-title: Tooltips
solution: Experience Manager
title: Tooltips
topic: Dynamic media
uuid: 4cf5ce32-136e-4612-b550-715d51cef982
---

# Tooltips{#tooltips}

On desktop systems some user interface elements like buttons have tool tips that are displayed on mouse hover.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS properties of the main viewer area**

The appearance of tool tips is controlled with the following CSS class selector:

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
>In case tool tip styles are customized from within the embedding web page, all properties have to contain `!IMPORTANT` rule. This is not necessary if tool tips are customized in the viewer's CSS file.

Example - to set up tool tips that have a gray border with a 3 pixel corner radius, black background, and white text in Arial, 11 pixels size:

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

