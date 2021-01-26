---
description: PageView.enableHD
solution: Experience Manager
title: PageView.enableHD
topic: Dynamic Media
uuid: 34c0e59f-4ed0-4b62-b661-aff20ff64ec4
---

# PageView.enableHD{#pageview-enablehd}

 [!DNL `[PageView.|<containerId>_pageView.]enableHD=always|never|limit[, *`number`*]`]

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Enable, limit or disable optimization for devices where <span class="codeph"> devicePixelRatio</span> is greater than <span class="codeph"> 1</span>, that is devices with high-density display like iPhone4 and similar devices. If active then the component limits the size of the IS image request as if the device only had a pixel ratio of <span class="codeph"> 1</span> and that way reducing the bandwidth. </p> <p>See example below </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> number</span></span> </p> </td> 
   <td colname="col2"> <p> If using the limit setting, the component enables high pixel density only up to the specified limit. </p> <p>See example below. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-38b878e38caa439bb462d4fa637afdaa}

Optional.

## Default {#section-50b22de303c1432094530e6583132c02}

`limit,1500`

## Example {#section-09433488774245d985acef6c0341ece0}

The following are the expected results when you use this configuration attribute with the viewer, and the viewer size is 1000 x 1000:

<table id="table_F97FEDA0EE1B4EF6AC9FF9060548ACA4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>If the set variable equals </p> </th> 
   <th colname="col2" class="entry"> <p>Result </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> always</span> </p> </td> 
   <td colname="col2"> <p>The pixel density of the screen/device is always taken into account. </p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>If the screen pixel density = 1, then the requested image is 1000 x 1000. </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>If the screen pixel density = 1.5, then the requested image is 1500 x 1500. </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>If the screen pixel density = 2, then the requested image is 2000 x 2000. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> never</span> </p> </td> 
   <td colname="col2"> <p>It always uses a pixel density of 1 and ignores the device's HD capability. Therefore, the requested image requested is always 1000 x 1000. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> limit&lt;number&gt;</span> </p> </td> 
   <td colname="col2"> <p>A device pixel density is requested and served only if the resulting image is below the specified limit. </p> <p>The limit number applies to either the width or the height dimension. </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>If the limit number is 1600, and the pixel density is 1.5, then the 1500 x 1500 image is served. </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>If the limit number is 1600, and the pixel density is 2, then the 1000 x 1000 image is served because the 2000 x 2000 image exceeds the limit. </p> </li> 
     </ul> </p> <p><b>Best practice</b>: The limit number needs to work in conjunction with the company setting for maximum size image. Therefore, set the limit number to equal the company maximum image size setting. </p> </td> 
  </tr> 
 </tbody> 
</table>

