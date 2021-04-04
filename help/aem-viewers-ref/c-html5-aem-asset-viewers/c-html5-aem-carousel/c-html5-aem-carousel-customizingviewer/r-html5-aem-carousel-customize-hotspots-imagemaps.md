---
description: The viewer displays hotspot icons over the main view in places where hotspots were originally authored in Dynamic Media of AEM Assets – on-demand.


solution: Experience Manager
title: Hotspots and Image maps

feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
exl-id: 70517201-9d59-4d9c-986d-a6e9655b7956
---
# Hotspots and Image maps{#hotspots-and-image-maps}

The viewer displays hotspot icons over the main view in places where hotspots were originally authored in Dynamic Media of AEM Assets – on-demand.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS properties of the main viewer area**

The appearance of the hotspot icon is controlled with the following CSS class selector:

```
.s7carouselviewer .s7imagemapeffect .s7icon
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
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Hotspot icon artwork. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>Position inside the artwork sprite, if CSS sprites are use. </p> <p>See <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Hotspot icon width. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hotspot icon height. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - set up a 56 x 56 pixels hotspot icon that displays a different image for each of the two different icon states:

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
 background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
 width: 56px; 
 height: 56px; 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
 background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

<!--<a id="section_26D0B8444D1F42D493793FF54968C0B9"></a>-->

**CSS properties of the image map region**

The appearance of the image map region is controlled with the following CSS class selector:

`.s7carouselviewer .s7imagemapeffect .s7region`

<table id="table_DAE7A78AA4A74DC78B2D94F29E8E236B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS property </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background </span> </p> </td> 
   <td colname="col2"> <p>Image map region fill color. </p> <p>Specify this color in <span class="codeph"> #RRGGBB </span>, <span class="codeph"> RGB(R,G,B) </span>, or <span class="codeph"> RGBA(R,G,B,A) </span> formats. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Image map region fill color. </p> <p>Specify this color in <span class="codeph"> #RRGGBB </span>, <span class="codeph"> RGB(R,G,B) </span>, or <span class="codeph"> RGBA(R,G,B,A) </span> formats. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p> Image map region border style. Should be specified as " <span class="codeph"> width </span> <span class="codeph"> solid color </span>", where <span class="codeph"> width </span> is expressed in pixels, and <span class="codeph"> color </span> is set as <span class="codeph"> #RRGGBB </span>, <span class="codeph"> RGB(R,G,B) </span>, or <span class="codeph"> RGBA(R,G,B,A) </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - set up a transparent image map region with a one pixel black border:

```
.s7carouselviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```
