---
description: Gets string values of system properties related to Image Portal.
seo-description: Gets string values of system properties related to Image Portal.
seo-title: getProperty
solution: Experience Manager
title: getProperty
uuid: 38ea08a6-c948-4a01-bc9a-d1609197224e
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
---

# getProperty{#getproperty}

Gets string values of system properties related to Image Portal.

 Supported system properties include:

* `IpsVersion`: IPS version number. 
* `IpsImageServerUrl`: Full, external URL prefix for the IPS Image Server. 
* `VideoRootUrl` 
* `swfRootUrl` 
* `SvgRenderRootUrl`: URL prefix for rendering SVG assets. 
* `SvgRenderEnabled`: True if SVG assets can be rendered by `SvgRenderRootUrl`. 

* `UploadPostMaxFileSize`: Maximum size (in bytes) of file data allowed in an upload [!DNL POST]. The system rejects files larger than the maximum limit.

## Authorized User Types {#section-2cd36bbd46ed414b8753569d5895530e}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `TrialSiteUser` 
* `ImagePortalAdmin` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-e3d389d183b244c2a5ef39c0ec331b5e}

**Input (getPropertyParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`name`*`  | `xsd:string`  | Yes  | The name of the property to get.  |

**Output (getPropertyReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`value`*`  | `xsd:string`  | Yes  | The property value.  |

## Examples {#section-3f80a78dd60c404181b34d3a912d7a36}

This code sample uses an IPS Properties string constant to return a specific value. In this example, the IPS property is the version of the IPS server.

**Request** 

```java
<ns1:getPropertyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:name>IpsVersion</ns1:name>
</ns1:getPropertyParam>
```

**Response** 

```java
<getPropertyReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <value>3.8.0</value>
</getPropertyReturn>
```

