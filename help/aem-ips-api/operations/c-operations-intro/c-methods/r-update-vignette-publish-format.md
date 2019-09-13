---
description: Updates the vignette publish format settings.
seo-description: Updates the vignette publish format settings.
seo-title: updateVignettePublishFormat
solution: Experience Manager
title: updateVignettePublishFormat
topic: Scene7 Image Production System API
uuid: ef8ae609-56e8-4ed6-906b-0668c5873946
index: y
internal: n
snippet: y
---

# updateVignettePublishFormat{#updatevignettepublishformat}

Updates the vignette publish format settings. 

## Authorized User Types {#section-2f2ad136d2884dc9bfef6da008196ed0}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-8c7ba8d2bce14071b21fccb11f44749f}

**Input (updateVignettePublishFormatParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`companyHandle`*`  | `xsd:string`  | Yes  | Company handle.  |
|  ` *`vignetteFormatHandle`*`  | `xsd:string`  | Yes  | Publish format handle.  |
|  ` *`name`*`  | `xsd:string`  | No  | Publish format name.  |
|  ` *`targetWidth`*`  | `xsd:int`  | Yes  | Specifies the target width of the resulting vignette view in pixels. Use zero so the output vignette has the same size as the master vignette.  |
|  ` *`targetHeight`*`  | `xsd:int`  | Yes  | Specifies the target height of the resulting vignette view in pixels. Use zero so the output vignette has the same size as the master vignette.  |
|  ` *`createPyramid`*`  | `xsd:boolean`  | Yes  | Creates a pyramid vignette optimized for zooming on the Image Rendering server. Starting at the maximum size, set by the Target Vignette Size fields, this creates multiple size views in a single vignette output file. Each subsequent view size is halved until the width and height are within 128x128 pixels.  |
|  ` *`thumbWidth`*`  | `xsd:int`  | Yes  | Specifies the width of each resulting thumbnail in pixels. This setting is optional. Leave as zero for no thumbnail file.  |
|  ` *`saveAsVersion`*`  | `xsd:int`  | Yes  | Specifies the file format for the published vignettes. Given a new version of Image Authoring and an older version of the Image Rendering Server, you must specify a vignette version that your ImageRendering Server can read. If you specify a higher version, the Image Rendering server cannot read the published vignettes. Set to zero to publish vignettes at the latest version.  |
|  ` *`sizeSuffixSeparator`*`  | `xsd:string`  | Yes  | Specifies the character that separates the vignette name and the suffix indicating its width.  |
|  ` *`sharpen`*`  | `xsd:int`  | No  | Applies sharpening to the main view image for each publish vignette size. Sharpening can compensate for blurring when the vignettes are scaled.  |
|  ` *`usmAmount`*`  | `xsd:double`  | Yes  | Digital unsharp masking is a flexible and powerful way to increase sharpness, especially in scanned images. This controls the magnitude of each overshoot (how much darker and lighter the edge borders become).  |
|  ` *`usmRadius`*`  | `xsd:double`  | Yes  | Affects the size of the edges to be enhanced or how wide the edge rims become, so a smaller radius enhances smaller-scale detail. Higher radius values can cause halos at the edges. Fine detail needs a smaller radius as tiny detail of the same size or smaller than the radius is lost.  |
|  ` *`usmThreshold`*`  | `xsd:int`  | Yes  | Controls the minimum brightness change to be sharpened or how far apart adjacent tonal values must be before the filter works. This setting can sharpen more pronouced edges while leaving more subtle edges untouched. The allowable range of threshold is 0 to 255.  |

**Output (updateVignettePublishFormatReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`vignetteFormatHandle`*`  | `xsd:string`  | Yes  | Handle to the updated vignette publish format.  |

## Example {#section-fcba4bf2b7264786a676e315a35dbe43}

This code sample updates a vignette publish format and returns the handle to the updated format.

**Request** 

```java
<updateVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|283</vignetteFormatHandle>
   <name>APIcreateVignettePublishFormat2</name>
   <targetWidth>1000</targetWidth>
   <targetHeight>800</targetHeight>
   <createPyramid>false</createPyramid>
   <thumbWidth>100</thumbWidth>
   <saveAsVersion>0</saveAsVersion>
   <sizeSuffixSeparator>-</sizeSuffixSeparator>
   <sharpen>50</sharpen>
   <usmAmount>240.0</usmAmount>
   <usmRadius>3.1</usmRadius>
   <usmThreshold>150</usmThreshold>
</updateVignettePublishFormatParam>
```

**Response** 

```java
<updateVignettePublishFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatHandle>v|21|283</vignetteFormatHandle>
</updateVignettePublishFormatReturn>
```

