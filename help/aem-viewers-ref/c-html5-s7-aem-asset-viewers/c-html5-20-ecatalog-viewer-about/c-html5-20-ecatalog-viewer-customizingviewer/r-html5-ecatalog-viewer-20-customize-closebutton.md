---
description: Clicking or tapping this button closes the containing web page. This button only appears if the closebutton parameter is set to 1. This button is not available on desktop systems. You can size, skin, and position this button by using CSS.
seo-description: Clicking or tapping this button closes the containing web page. This button only appears if the closebutton parameter is set to 1. This button is not available on desktop systems. You can size, skin, and position this button by using CSS.
seo-title: Close button
solution: Experience Manager
title: Close button
uuid: b0de1600-6b02-4b59-aac6-ade0ec6dc087
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
---

# Close button{#close-button}

Clicking or tapping this button closes the containing web page. This button only appears if the closebutton parameter is set to 1. This button is not available on desktop systems. You can size, skin, and position this button by using CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS properties of the main viewer area**

The appearance of the button is controlled with the following CSS class selector:

`.s7ecatalogviewer .s7closebutton`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS property </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Position from the top border of the main control bar, including padding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p>Position from the right border of the main control bar, including padding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p>Position from the left border of the main control bar, including padding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>Position from the bottom border of the main control bar, including padding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Width of the button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Height of the button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>The image that is displayed for a given button state. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position inside artwork sprite, if CSS sprites are used. </p> <p>See also <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>This button supports the `state` attribute selector, which you can use to apply different skins to different button states.

The button tool tip can be localized. See [Localization of user interface elements](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) for more information.

Example - to set up a close button that is 56 x 56 pixels, positioned 4 pixels from the top and right edge of the main control bar, and displays a different image for each of the four different button states.

```
.s7ecatalogviewer .s7closebutton { 
top:4px; 
right:4px; 
width:56px; 
height:56px; 
} 
.s7ecatalogviewer .s7closebutton [state='up'] { 
background-image:url(images/v2/CloseButton_dark_up.png); 
} 
.s7ecatalogviewer .s7closebutton [state='over'] {  
background-image:url(images/v2/CloseButton_dark_over.png); 
} 
.s7ecatalogviewer .s7closebutton [state='down'] {  
background-image:url(images/v2/CloseButton_dark_down.png); 
} 
.s7ecatalogviewer .s7closebutton [state='disabled'] { 
background-image:url(images/v2/CloseButton_dark_disabled.png); 
}
```

