---
description: Sets various company-specific configuration values.
solution: Experience Manager
title: setCompanySettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c6b72ceb-3c86-4b13-89e9-5f1bb9846b2c
TQID: https://experienceleague.adobe.com/1Q3p0WcorxVYyzW2kc06qcThKqc-ffsI6AwNxAwQEbs
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
---
# setCompanySettings{#setcompanysettings}

Sets various company-specific configuration values.

 Syntax 

## Authorized User Types {#section-41732fa7424b455cb458eec21a02259c}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-a472da6c57c74a94a179dda081004888}

**Input (setCompanySettingsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | Company handle.  |
|  overwriteMode  | `xsd:string`  | No  | Asset overwrite mode.  |
|  retainPublishState  | `xsd:boolean`  | No  |Set to `true` to preserve the publish state when an asset is re-uploaded.  |
|  defaultSourceProfileHandle  | `xsd:string`  | No  | IccProfile asset to use as default source color profile.  |
|  defaultDisplayProfileHandle  | `xsd:string`  | No  | IccProfile asset to use as default display color profile.  |
|  iptcExifMappingXsltHandle  | `xsd:string`  | No  | XSL asset used for mapping IPTC and EXIF metadata to IPS metadata fields.  |
|  xmpMappingXsltHandle  | `xsd:string`  | No  | XSL asset used to map XMP metadata to IPS metadata fields.  |
|  diskSpaceWarningMin  | `xsd:int`  | No  | Minimum free disk space (in KB) available before a warning message is sent.  |
|  emailTrashCleanupWarning  | `xsd:boolean`  | No  |Set to `true` to send company administrators a notification whenever assets are emptied from trash.  |

**Output (setCompanySettingsReturn)**

The IPS API does not return a response for this operation.

## Examples {#section-d10bf1d3d86f46f7bcf78dc1a2c363c5}

This code sample sets a company's configuration.

**Request** 

```java
<ns1:setCompanySettingsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <ns1:companyHandle>c|6</ns1:companyHandle>
   <ns1:overwriteMode>OverwriteFullName</ns1:overwriteMode>
   <ns1:retainPublishState>true</ns1:retainPublishState>
   <ns1:diskSpaceWarningMin>100000</ns1:diskSpaceWarningMin>
   <ns1:emailTrashCleanupWarning>true</ns1:emailTrashCleanupWarning>
</ns1:setCompanySettingsParam>
```

**Response**

None.
