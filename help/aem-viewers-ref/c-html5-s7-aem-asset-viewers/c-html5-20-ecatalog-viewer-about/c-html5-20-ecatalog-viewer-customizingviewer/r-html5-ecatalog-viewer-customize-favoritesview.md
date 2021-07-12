---
description: Favorites view consists of a column of thumbnail images.


solution: Experience Manager
title: Favorites view

feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 10536242-1015-49ff-ae27-59671f30d886
---
# Favorites view{#favorites-view}

Favorites view consists of a column of thumbnail images.

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

The appearance of the Favorites view container is controlled with the following CSS class selector:

```
.s7ecatalogviewer .s7favoritesview
```

The position and the height of the Favorites view is managed by the view; in CSS it is only possible to define the width.

**CSS properties of the Favorites view**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Background color of the Favorites view. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Width of the view. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set up a Favorites view that is 100 pixels wide with a semi-transparent grey background.

```
.s7ecatalogviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

The spacing between Favorites thumbnails is controlled with the following CSS class selector:

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell
```

**CSS properties of the Favorites thumbnails**

<table id="table_EED8CE63D805458196DE0E87C7E9945F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> The size of the vertical margin around each thumbnail. The actual thumbnail spacing is equal to the sum of the top and bottom margin that is set for <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set up 10 pixel spacing.

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

The appearance of individual thumbnail is controlled with the following CSS class selector:

```
.s7ecatalogviewer .s7favoritesview .s7thumb
```

**CSS properties of the Favorites thumbnails**

<table id="table_6F5B1438CAFA49E9B33400C6970ABDA1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Width of the thumbnail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Height of the thumbnail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Border of the thumbnail. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumbnail supports the `state` attribute selector,which can be used to apply different skins to different thumbnail states. In particular, `state="selected"` corresponds to the thumbnail recently selected by the user. `state="default"` corresponds to the rest of the thumbnails. And `state="over"` is used on mouse hover.

Example - to set up thumbnails that are 75 x 75 pixels, have a light grey default border, and a dark grey selected border.

```
.s7ecatalogviewer .s7favoritesview .s7thumb { 
 width: 75px; 
 height: 75px;  
} 
.s7ecatalogviewer .s7favoritesview .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7ecatalogviewer .s7favoritesview .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

The appearance of the thumbnail label is controlled with the following CSS class selector:

```
.s7ecatalogviewer .s7favoritesview .s7label
```

**CSS properties of the Favorites label**

<table id="table_B41339A16ACB46CB87D3EB1FD05FA2CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-famiy </span> </p> </td> 
   <td colname="col2"> <p>Font name. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Font size. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set up labels with a 14 pixel Helvetica font.

```
.s7ecatalogviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```
