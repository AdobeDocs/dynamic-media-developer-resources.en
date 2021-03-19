---
description: Parameter common to all viewers.
seo-description: Parameter common to all viewers.
seo-title: asset
solution: Experience Manager
title: asset
uuid: 6a72257f-d204-4258-b6f8-de6f7b00fd54
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,Business Practitioner
---

# asset{#asset}

Parameter common to all viewers.

 ` asset= *`assetId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> assetId </span> </span> </p> </td> 
   <td colname="col2"> <p> The asset ID of the single video or Adaptive Video Set. </p> </td> 
  </tr> 
 </tbody> 
</table>

This property is required, unless `video` parameter is used. See [External Video Support](../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3) under Video or [External video support](../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) under Video360.

or

` asset= *`image`*`

<table id="table_67E18F42E97C4AAAB0A2F67B7924765D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> image </span> </span> </p> </td> 
   <td colname="col2"> <p> Specifies a single image or a carousel set. Apply double HTTP encoding to any unsafe character that exists in the image name or the carousel set name. </p> </td> 
  </tr> 
 </tbody> 
</table>

or

` asset= *`image`* | *`imageList`* | *`imageListWithModifiers`* | *`multiDimensionalSpinSet`* [%3F *`modifiers`*]`

<table id="table_A2A0ACD942E942BC99AF0DC80FB1C670"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> image </span> </span> </p> </td> 
   <td colname="col2"> <p> Specifies a single image. Apply double HTTP encoding to any unsafe character that exists in the image name. </p> <p>Or, specifies a reference to an image set. The viewer retrieves image sets from the server, using <span class="codeph"> req=set IS </span> request. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imageList </span> </span> </p> </td> 
   <td colname="col2"> <p> Specifies an explicit image set, consisting of a sorted sequence of items, or frames, separated by commas. </p> <p> <p>Note:  This feature is supported in Adobe Dynamic Media Classic; it is not supported in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imageListWithModifiers </span> </span> </p> </td> 
   <td colname="col2"> <p> Specifies an explicit image set where each frame has its own Image Serving modifiers. In this case, the list of frames are wrapped within parentheses. Make sure you apply double HTTP encoding to any comma that is present in the frame-specific Image Serving modifier. </p> <p> <p>Note:  This feature is supported in Adobe Dynamic Media Classic; it is not supported in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> multiDimensionalSpinSet </span> </span> </p> </td> 
   <td colname="col2"> <p>Specifies an explicit multi-dimensional spin set using the following syntax: </p> <p> <span class="codeph"> (( <span class="varname"> horizontalSpinSet </span>)[,( <span class="varname"> horizontalSpinSet </span>)]) </span> </p> <p> where <span class="codeph"> <span class="varname"> horizontalSpinSet </span> </span> is a comma-separated list of frames for a given horizontal axis. All <span class="codeph"> <span class="varname"> horizontalSpinSet </span> </span> should have the same number of frames. </p> <p> <p>Note:  This feature is supported in Adobe Dynamic Media Classic; it is not supported in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> modifiers </span> </span> </p> </td> 
   <td colname="col2"> <p> Image Serving commands; <span class="codeph"> &amp; </span> and <span class="codeph"> = </span> separators must be HTTP-encoded as <span class="codeph"> %26 </span> and <span class="codeph"> %3D </span>, respectively. </p> </td> 
  </tr> 
 </tbody> 
</table>

or

` asset=( *`mediaSet`* | ( *`video`*; *`swatchId`* | *`image`*; *`swatchId`* | *`setId`*; *`swatchId`*); *`ID`*;( *`video`*; *`swatchId`* | *`image`*; *`swatchId`* | *`setId`*; *`swatchId`*); *`ID`*;] [%3F *`modifiers`*]`

<table id="table_D31C8507C02A4452A79DEDDEC62EF2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> mediaSet </span> </span> </p> </td> 
   <td colname="col2"> <p> Specifies a reference to a media set. The viewer retrieves media sets from the server, using req=set IS request. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> video </span> </span> </p> </td> 
   <td colname="col2"> <p> Single video or Adaptive Video Set. </p> <p> <p>Note:  This feature is supported in Adobe Dynamic Media Classic; it is not supported in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> image </span> </span> </p> </td> 
   <td colname="col2"> <p> Single image. </p> <p> <p>Note:  This feature is supported in Adobe Dynamic Media Classic; it is not supported in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> setId </span> </span> </p> </td> 
   <td colname="col2"> <p> Swatch set. </p> <p> <p>Note:  This feature is supported in Adobe Dynamic Media Classic; it is not supported in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> swatchId </span> </span> </p> </td> 
   <td colname="col2"> <p>Swatch image. </p> <p> <p>Note:  This feature is supported in Adobe Dynamic Media Classic; it is not supported in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ID </span> </span> </p> </td> 
   <td colname="col2"> <p> Media Set item type identifier can be one of the following: </p> <p> 
     <ul id="ul_3100F9356628498DA820C07F6F69CC9B"> 
      <li id="li_51B649A539F14510873CFDA85A6AA714"> <p> <span class="codeph"> advanced_image </span> </p> <p>For single image. </p> </li> 
      <li id="li_7E764D67294647C1A828F949E5ED1908"> <p> <span class="codeph"> advanced_swatchset </span> </p> <p>For nested swatch set. </p> </li> 
      <li id="li_C942CED779B54110BCDC74188995FD5B"> <p> <span class="codeph"> spin </span> </p> <p>For spin set. </p> </li> 
      <li id="li_6EA5C54F078D4B24B44F1588BF083842"> <p> <span class="codeph"> video </span> </p> <p>For single video. </p> </li> 
      <li id="li_8110FA7E0CAB4681A2D8C15F2A656E69"> <p> <span class="codeph"> video_set </span> </p> <p>For Adaptive Video Sets. </p> </li> 
     </ul> </p> <p> <p>Note:  This feature is supported in Adobe Dynamic Media Classic; it is not supported in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> modifiers </span> </span> </p> </td> 
   <td colname="col2"> <p> Image Serving commands; <span class="codeph"> &amp; </span> and <span class="codeph"> = </span> separators must be HTTP-encoded as <span class="codeph"> %26 </span> and <span class="codeph"> %3D </span>, respectively. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Images that use IR (Image Rendering) or UGC (User-Generated Content) are not supported by this viewer.

## Properties {#section-10ee45d637134e0fbcd943c62578cb78}

Required.

## Default {#section-d411e450028c460392cb8508f8ccc5d9}

None.

## Examples {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

Single asset reference:

```
asset=Scene7SharedAssets/Backpack_B
```

or

```
asset=/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg
```

or

```
asset=/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4
```

or

```
asset=/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner
```

or

```
asset=Viewers/space_station_360-AVS
```

Single reference to an image set that is defined in a catalog:

```
asset=Viewers/Pluralist
```

Explicit image set:

```
asset=Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C
```

Explicit image set with frame-specific Image Serving modifiers:

```
asset=(Scene7SharedAssets/Backpack_B%3Fop_colorize%3D255%252C0%252C0,Scene7SharedAssets/Backpack_B%3Fop_colorize%3D0x00ff00)
```

Single reference to a spin set that is defined in a catalog:

```
asset=Scene7SharedAssets/SpinSet-Sample
```

Explicit spin set:

```
asset=Scene7SharedAssets/Frame-1,Scene7SharedAssets/Frame-2,Scene7SharedAssets/Frame-3,Scene7SharedAssets/Frame-4,Scene7SharedAssets/Frame-5,Scene7SharedAssets/Frame-6,Scene7SharedAssets/Frame-7,Scene7SharedAssets/Frame-8
```

Explicit multi-dimensional spin set:

```
asset=((Scene7SharedAssets/ring1-25,Scene7SharedAssets/ring1-26,Scene7SharedAssets/ring1-27,Scene7SharedAssets/ring1-28,Scene7SharedAssets/ring1-29,Scene7SharedAssets/ring1-30,Scene7SharedAssets/ring1-31,Scene7SharedAssets/ring1-32,Scene7SharedAssets/ring1-33,Scene7SharedAssets/ring1-34,Scene7SharedAssets/ring1-35,Scene7SharedAssets/ring1-36),(Scene7SharedAssets/ring1-13,Scene7SharedAssets/ring1-14,Scene7SharedAssets/ring1-15,Scene7SharedAssets/ring1-16,Scene7SharedAssets/ring1-17,Scene7SharedAssets/ring1-18,Scene7SharedAssets/ring1-19,Scene7SharedAssets/ring1-20,Scene7SharedAssets/ring1-21,Scene7SharedAssets/ring1-22,Scene7SharedAssets/ring1-23,Scene7SharedAssets/ring1-24),(Scene7SharedAssets/ring1-01,Scene7SharedAssets/ring1-02,Scene7SharedAssets/ring1-03,Scene7SharedAssets/ring1-04,Scene7SharedAssets/ring1-05,Scene7SharedAssets/ring1-06,Scene7SharedAssets/ring1-07,Scene7SharedAssets/ring1-08,Scene7SharedAssets/ring1-09,Scene7SharedAssets/ring1-10,Scene7SharedAssets/ring1-11,Scene7SharedAssets/ring1-12))
```

Single mixed media set reference:

```
 asset=Scene7SharedAssets/Mixed_Media_Set_Sample
```

Explicit mixed media set:

```
asset=Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;
```

Sharpening modifier added to all images in the set:

```
asset=Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C%3Fop_sharpen=%3D1
```

```
asset=Scene7SharedAssets/Mixed_Media_Set_Sample%3Fop_sharpen%3D1
```

```
asset=Viewers/Pluralist%3Fop_sharpen%3D1
```

