---
description: Creates a new publish format for a vignette.
seo-description: Creates a new publish format for a vignette.
seo-title: createVignettePublishFormat
solution: Experience Manager
title: createVignettePublishFormat
topic: Dynamic Media Image Production System API
uuid: 834ebe6a-e105-4075-8004-172237980933
---

# createVignettePublishFormat{#createvignettepublishformat}

Creates a new publish format for a vignette.

Vignette formats specify the size of published vignettes and their thumbnails, as well as zoom levels, sharpening parameters, and the file format version for vignettes produced from primary vignettes published to an Image Rendering server from IPS.

Newer Image Rendering server versions can support pyramid vignettes, which eliminates the need to define specific vignette format sizes for publishing.

## Authorized User Types {#section-f5c563e3695c4dba8df41e2a965aace7}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-3a368186ec1d4005bca056fc9d9bacc7}

**Input (createVignettePublishFormatParam)** 

<table id="table_4D5B2913FA784EC09190F25223C1A680"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Required </th> 
   <th colname="col4" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> Handle to the company the vignette belongs to. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> Name to identify the vignette publishing format. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> <p>Specifies the target width of the resulting vignette view in pixels. </p> <p>Use zero so the output vignette has the same size as the primary vignette. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetHeight</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> Creates a pyramid vignette optimized for zooming on the Image Rendering server. Starting at the maximum size, set by the Target Vignette Size fields, this creates multiple size views in a single vignette output file. Each subsequent view size is halved until the width and height are within 128x128 pixels. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createPyramid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> Specifies the width of each resulting thumbnail in pixels. This setting is optional. Leave as zero for no thumbnail file. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> Specifies the file format for the published vignettes. Given a new version of Image Authoring and an oler version of the Image Rendering Server, you must specify a vignette version that your ImageRendering Server can read. If you specify a higher version, the Image Rendering server cannot read the published vignettes. Set to zero to publish vignettes at the latest version. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> saveAsVersion</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> Specifies the character the separates the vignette name and the suffix indicating its width. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sizeSuffixSeparator</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> Specifies the character the separates the vignette name and the suffix indicating its width. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sharpen</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Applies sharpening to the main view image for each puvlish vignette size Sharpening can compensate for blurring when the vignetters are scaled. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmAmount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> Digital unsharp masking is a flexible and powerful way to increase sharpness, especially in scanned images. This controls the magnitude of each overshoot (how much darker and light the edge borders become). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmRadius</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> Affects the size of the edges to be enhanced or how wide the edge rims become, so a smaller radium enhances smaller-scalle detail. Higher radius values can cause halos at the edges. Fine detail needs a smaller radius as tiny detail of the same size or smaller than the radius is lost. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmThreshold</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> Controls the minimum brightness change to be sharpened or how far apart adjacent tonal values must be before the filter works. This setting can sharpen more pronouced edges while leaving more subtle edges untouched. THe allowable range of threshold of 0 to 255. </td> 
  </tr> 
 </tbody> 
</table>

**Output (createVignettePublishFormatReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`vignetteFormatHandle`*`  | `xsd:string`  | Yes  | The handle to the created vignette format.  |

## Examples {#section-0564752d439642b9bb8de2903db6de1e}

This code creates vignette publish format. The creation request specifies a name, target width and height, and other required values.

**Request** 

```java
<createVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <name>APIcreateVignettePublishFormat1</name>
   <targetWidth>1200</<targetWidth>
   <targetHeight>800</targetHeight>
   <createPyramid>true</createPyramid>
   <thumbWidth>400</thumbWidth>
   <saveAsVersion>0</saveAsVersion>
   <sizeSuffixSeparator>-</sizeSuffixSeparator>
   <sharpen>50</sharpen>
   <usmAmount>230.0</usmAmount>
   <usmRadius>1.1</usmRadius>
   <usmThreshold>130</usmThreshold>
</createVignettePublishFormatParam>
```

**Response** 

```java
<createVignettePublishFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</createVignettePublishFormatReturn>
```

