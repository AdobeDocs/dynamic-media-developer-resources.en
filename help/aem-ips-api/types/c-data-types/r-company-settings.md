---
description: Company-specific configuration settings.
seo-description: Company-specific configuration settings.
seo-title: CompanySettings
solution: Experience Manager
title: CompanySettings
topic: Scene7 Image Production System API
uuid: a807d5c1-058d-4313-b4f8-6ee203284003
index: y
internal: n
snippet: y
---

# CompanySettings{#companysettings}

Company-specific configuration settings.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  ` *`overwriteMode`*`  | `xsd:string`  | Determines whether to overwrite images in current folder with same base image name and extension.  |
|  ` *`retainPublishState`*`  | `xsd:boolean`  | Specifies whether a replacement image uploaded into IPS should retain the existing “Ready to Publish” setting or whether it should be as specified by the upload.  |
|  ` *`defaultSourceProfile`*`  | `types:Asset`  | Specifies the default source color profile (Coated FOGRA27 (ISO 126472:2004)) automatically applied as part of the “Use default Color Behavior”when adding CMYK image files.  |
|  ` *`defaultDisplayProfile`*`  | `types:Asset`  | Specifies the default internal color profile (U.S. Web Coated (SWOP) v2)automatically applied as part of the “Use default Color Behavior” when adding CMYK image files.  |
|  ` *`iptcExifMappingXslt`*`  | `types:Asset`  | The extraction of IPTC and EXIF image header data into IPS requires a conversion from internal field names to user-defined field names for the company. Determines an XSL translation table (default is “Do not extract any IPTC or EXIF fields”) for uploaded images.  |
|  ` *`xmpMappingXslt`*`  | `types:Asset`  | The extraction of XMP image header data into IPS requires a conversion from internal field names to user-defined field names for the company. Determines an XSL translation table (default is “Do not extract any XMP fields”) for uploaded images.  |
|  ` *`diskSpaceWarningMin`*`  | `xsd:int`  | Minimum amount of image directory free disk space before a warning is sent out.  |
|  ` *`emailTrashCleanupWarning`*`  | `xsd:boolean`  | Determines whether to send emails before items placed into the trash can are automatically deleted.  |
|  ` *`javascriptUploadEnabled`*`  | `types:Asset`  | Determines whether to upload JavaScript files. This is a potential security risk, so use this option with care.  |

