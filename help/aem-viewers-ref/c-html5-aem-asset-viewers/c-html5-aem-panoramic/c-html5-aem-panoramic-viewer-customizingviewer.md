---
title: Customizing Panoramic Viewer
description: All visual customization and most behavior customization for the Panoramic Viewer is done by creating a custom CSS.
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: c9dda4e8-2781-4870-9ccb-707823c56490
---
# Customizing Video360 Viewer{#customizing-video-viewer}

All visual customization and most behavior customization is done by creating a custom CSS.

The suggested workflow is to take the default CSS file for the appropriate viewer, copy it to a different location, customize it, and specify the location of the customized file in the `style=` command.

Default CSS files can be found at the following location:

`<s7viewers_root>/html5/PanoramicViewer.css`

Custom CSS file must contain the same class declarations as the default one. If a class declaration is omitted, the viewer does not function properly because it does not provide built-in default styles for user interface elements.

Alternative way to provide custom CSS rules is to use embedded styles directly on the web page or in one of linked external CSS rules.

When creating custom CSS keep in mind that the viewer assigns `.s7panoramicviewer` class to its container DOM element. If you are using external CSS file passed with `style=` command, use `.s7panoramicviewer` class as parent class in descendant selector for your CSS rules. If you are doing embedded styles on the web page, additionally qualify this selector with an ID of the container DOM element as follows: 

`#<containerId>.s7panoramicviewer.`


## General styling notes and advice {#section-95855dccbbc444e79970f1aaa3260b7b}

* All paths to external assets within CSS are resolved against the CSS location, not the viewer HTML page location. Take this into account when copying the default CSS to a different location: it may be necessary to either copy the default assets as well or to update paths within the custom CSS.
* You can use various formats for color value supported by CSS. If transparency is needed, `rgba(R,G,B,A)` format is suggested. Otherwise, transparency is not required `#RRGGBB` can be used.

When customizing viewer UI with CSS the use of `!IMPORTANT` rule is not supported to style viewer elements. In particular, `!IMPORTANT` rule should not be used to override any default or run-time styling provided by the viewer or Viewer SDK as it may affect proper components behavior. Instead, CSS selectors with proper specificity should be used to set CSS properties documented in this reference guide.

## Panoramic Viewer CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

**Main viewer area**
The main view area is the area occupied by the panoramic image.  It usually sets to fit the available device screen when no size is specified.

The appearance of the viewing area is controlled with the CSS class selector:
`.s7panoramicviewer`

Applicable CSS properties include:

<table id="table_panA68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> the width of the viewer; </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> the height of the viewer; </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Example:
To set up a viewer with size 1024 x 512 pixels.

```
.s7panoramicviewer {
	width: 1024px;
	height: 500px;	
}
```

**Panoramic View**
Main view consists of the panoramic image. 

The appearance of the main view is controlled with the CSS class selector:
`.s7panoramicviewer .s7panoramicview`

Applicable CSS properties include:
<table id="table_pann68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> the background color of the main view; </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Example:
To make main view transparent:

```
.s7panoramicviewer .s7panoramicview {
	background-color: transparent;
}
```
