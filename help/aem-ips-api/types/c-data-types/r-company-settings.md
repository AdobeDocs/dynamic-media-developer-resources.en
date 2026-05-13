---
description: Company-specific configuration settings.
solution: Experience Manager
title: CompanySettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82e6362d-beab-47ff-bb20-11047f0d8787
TQID: 'https://experienceleague.adobe.com/iGc-AwCFbpkATjLjvSBtx4vsP0-OUDSkH2dFHZ-j2rg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
---
# [!DNL CompanySettings]{#companysettings}

Company-specific configuration settings.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  overwriteMode  | `xsd:string`  | Determines whether to overwrite images in the current folder with the same base image name and extension.  |
|  retainPublishState  | `xsd:boolean`  | Specifies whether a replacement image uploaded into IPS should retain the existing "Ready to Publish" setting or whether it should be as specified by the upload.  |
|  defaultSourceProfile  | `types:Asset`  | Specifies the default source color profile (Coated FOGRA27 (ISO 126472:2004)) automatically applied as part of the "Use default Color Behavior"when adding CMYK image files.  |
|  defaultDisplayProfile  | `types:Asset`  | Specifies the default internal color profile (U.S. Web Coated (SWOP) v2)automatically applied as part of the "Use default Color Behavior" when adding CMYK image files.  |
|  iptcExifMappingXslt  | `types:Asset`  | The extraction of IPTC and EXIF image header data into IPS require a conversion from internal field names to user-defined field names for the company. Determines an XSL translation table (default is "Do not extract any IPTC or EXIF fields") for uploaded images.  |
|  xmpMappingXslt  | `types:Asset`  | The extraction of XMP image header data into IPS requires a conversion from internal field names to user-defined field names for the company. Determines an XSL translation table (default is "Do not extract any XMP fields") for uploaded images.  |
|  diskSpaceWarningMin  | `xsd:int`  | Minimum amount of image directory free disk space before a warning is sent out.  |
|  emailTrashCleanupWarning  | `xsd:boolean`  | Determines whether to send emails before trash can items are automatically deleted.  |
|  javascriptUploadEnabled  | `types:Asset`  | Determines whether to upload JavaScript files. This option is a potential security risk, so use with care.  |
