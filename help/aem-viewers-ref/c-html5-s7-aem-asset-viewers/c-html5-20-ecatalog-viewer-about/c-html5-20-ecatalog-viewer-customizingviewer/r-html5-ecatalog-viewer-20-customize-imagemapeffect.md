---
description: Depending on the value of the mode parameter, the viewer displays image map icons over the main view in places where maps are originally authored in Scene7 Publishing System or renders exact regions that match the shape of original image maps.
seo-description: Depending on the value of the mode parameter, the viewer displays image map icons over the main view in places where maps are originally authored in Scene7 Publishing System or renders exact regions that match the shape of original image maps.
seo-title: Image map effect
solution: Experience Manager
title: Image map effect
topic: Dynamic media
uuid: 193d2f4e-77a2-4741-bf36-90ca31c600c6
---

# Image map effect{#image-map-effect}

Depending on the value of the mode parameter, the viewer displays image map icons over the main view in places where maps are originally authored in Scene7 Publishing System or renders exact regions that match the shape of original image maps.

<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>

**CSS properties of the main viewer area**

The appearance of the image map icon is controlled with the following CSS class selector:

```
.s7ecatalogviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>The `s7mapoverlay` CSS class used to style image map icons in the past is now deprecated; use `s7icon` instead.

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS property </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Image map icon artwork. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position inside artwork sprite, if CSS sprites are used. </p> <p>See also <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Image map icon width in pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Image map icon height in pixels. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Image map icon supports the `state` attribute selector, which you can use to apply different skins to the icon states of `default` and `active`.

Example - set up a 28 x 28 pixels image map icon that displays a different image for each of the two different icon states.

```
.s7ecatalogviewer .s7imagemapeffect .s7icon { 
 height: 28px; 
 width: 28px;  
 background-image: url(images/v2/ImageMapEffect_dark_up.png); 
} 
.s7ecatalogviewer .s7imagemapeffect .s7icon[state="default"] { 
 opacity: 0.5; 
} 
.s7ecatalogviewer .s7imagemapeffect .s7icon[state="active"] { 
opacity: 1; 
}
```

See also [Image map support](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-image-map-support.md#concept-28759efae5014a1fa8b0fb14dc26812a).

The appearance of the image map region is controlled with the following CSS class selector:

```
.s7ecatalogviewer .s7imagemapeffect .s7region
```

<table id="table_1FF98CE842604AAABD838FF528CDC4EF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS property </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background </span> </p> </td> 
   <td colname="col2"> <p> Image map region fill color. </p> <p>Specified in #RRGGBB, RGB(R,G,B), or RGBA(R,G,B,A) format. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Image map region fill color. </p> <p>Specified in #RRGGBB, RGB(R,G,B) or RGBA(R,G,B,A) format. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p> Image map region border style. </p> <p>Specified as <span class="codeph"> <span class="varname"> width </span> solid <span class="varname"> color </span> </span>, where <span class="codeph"> <span class="varname"> width </span> </span> is expressed in pixels and <span class="codeph"> <span class="varname"> color </span> </span> is set as #RRGGBB, RGB(R,G,B) or RGBA(R,G,B,A). </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - set up a transparent image map region with `1` pixel black border :

```
.s7ecatalogviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```

