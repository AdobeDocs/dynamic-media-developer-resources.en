---
description: Returns IPS settings for a specific company.
seo-description: Returns IPS settings for a specific company.
seo-title: getCompanySettings
solution: Experience Manager
title: getCompanySettings
topic: Scene7 Image Production System API
uuid: a41a50aa-45b3-4c38-bd06-e20dd99216e1
index: y
internal: n
snippet: y
---

# getCompanySettings{#getcompanysettings}

Returns IPS settings for a specific company.

 Syntax 

## Authorized User Types {#section-3378c9c67029473a87d5f5d8c616b1f3}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-e146f479c2744baa8f68be8c8848c97f}

**Input (getCompanySettingsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company whose settings you wish to retrieve.  |

**Output (getCompanySettingsReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`settings`*`  | `types:CompanySettings`  | Yes  | Company settings.  |

## Examples {#section-191f78995ecf473a95eadf7296204fd7}

This code sample returns all IPS settings for a specific company.

**Request** 

```java
<ns1:getCompanySettingsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <ns1:companyHandle>c|6</ns1:companyHandle>
</ns1:getCompanySettingsParam>
```

**Response** 

```java
<getCompanySettingsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <settings>
      <metadataArray>
         <items>
            <name>Profile Class</name>
            <value>1</value>
            <longVal>1</longVal>
         </items>
         <items>
             <name>Default Color Profile</name>
             <value>1</value>
         </items>
      </metadataArray>
      <iccProfileInfo>
         <originalPath>Scene7SharedAssets/ICCColorProfiles/Adobe ICC Profiles/RGB Profiles/</originalPath>
         <originalFile>sRGB Color Space Profile.icm</originalFile>
         <fileSize>0</fileSize>
      </iccProfileInfo>
      </defaultDisplayProfile>
      <diskSpaceWarningMin>100000</diskSpaceWarningMin>
      <emailTrashCleanupWarning>true</emailTrashCleanupWarning>
   </settings>
</getCompanySettingsReturn>
```
