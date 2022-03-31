---
title: KnockoutBackgroundOptions
description: Mask (knock-out) the background for selected images. This data type lets you overlay them in other layers with a transparency outside of subject image. An optional parameter that is off by default.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: aed8cf2e-5a09-43ff-9420-0d0d54059515
---
# KnockoutBackgroundOptions{#knockoutbackgroundoptions}

Mask (knock-out) the background for selected images. This data type lets you overlay them in other layers with a transparency outside of the subject image. 

This data type is optional and off by default.

 `KnockoutBackgroundOptions=[corner, tolerance, fill]` 

## Parameters {#section-3149b49ccb714e6eafa6655354816819}

>[!IMPORTANT]
>
>If you are configuring `KnockoutBackgroundOptions` in Adobe Experience Manager, use the following parameters instead: 
>* `kbCorner`
>* `kbTolerance`
>* `kbFillMethod` 
>
>For example: `KnockoutBackgroundOptions=kbCorner=UpperLeft&kbTolerance=0.2&kbFillMethod=MatchPixel`

<table id="table_68131DE0A3C84908A43C6F7777F20973"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> corner</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Selects the corner that you want to work with. <span class="codeph"> corner</span> accepts these values: 
    <ul id="ul_36C2F07706764A7081010D5521BF3096">
     <li id="li_CBACE5C6AA8C48D3BEE033D3AE03AF3C"><span class="codeph"> UpperLeft</span></li>
     <li id="li_49AC53536B4B4D2CA3DD89E2A2B2E95D"><span class="codeph"> BottomLeft</span></li>
     <li id="li_7AD372FF4A9B48F0A16964EE9CB3EE88"><span class="codeph"> UpperRight</span></li>
     <li id="li_D31476DD9A8E4BDBB13A6DDA46547877"><span class="codeph"> BottomRight</span></li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tolerance</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3">An optional setting that removes white space from image edges based on transparency. Accepts a range of values from 0.0 to 1.0. Specify: 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0 to match colors exactly. </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1 to enable the most color differences. </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fillMethod</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Control pixel transparency in the location specified by the <span class="codeph"><span class="varname"> corner</span></span> variable. The <span class="codeph"> fillMethod</span> accepts these values: </p> 
    <ul id="ul_D95F3B613D344BB89487ED09D83F9217"> 
     <li id="li_3D7B7CA1B9094D16A98E0BA3D962E97F"> <span class="codeph"> FloodFill</span>: Turns all pixels in the specified corner transparent. </li> 
     <li id="li_F97343C3DA7644BCBD1748AD8F9DCE2E"> <span class="codeph"> MatchPixel</span>: Turns all matching pixels transparent regardless of location. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Example {#section-3f9edfff321a4e4394f766298b9e284d}

```
<complexType name="KnockoutBackgroundOptions">
        <sequence>
            <!-- corner one of UpperLeft, BottomLeft, UpperRight, BottomRight -->
            <element name="corner" type="xsd:string" minOccurs="1"/>
            <!-- Tolerance real value between 0.0 and 1.0 -->
            <element name="tolerance" type="xsd:double" minOccurs="0"/>
            <!-- one of FloodFill or MatchPixel is required -->
            <element name="fillMethod" type="xsd:string" minOccurs="1"/>
        </sequence>
    </complexType>
```

## Used By {#section-28c43baafe85434a9ee9e303ed10569a}

The `KnockoutBackgroundOptions` type is used by:

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6) 
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) 
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)
