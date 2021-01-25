---
description: Returns information about a company's structure (number of files, etc.).
seo-description: Returns information about a company's structure (number of files, etc.).
seo-title: getDiskUsage
solution: Experience Manager
title: getDiskUsage
topic: Dynamic Media Image Production System API
uuid: 29190200-8f49-4689-9782-1df665dca1b7
---

# getDiskUsage{#getdiskusage}

Returns information about a company's structure (number of files, etc.).

## Authorized User Types {#authorized-user-types}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-e7e47082faf44ae28a2cfa7ef53aedbb}

**Input (getDiskUsageParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company whose disk usage you want to obtain.  |

**Output (getDiskUsageReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`diskUsageArray`*`  | `types:DiskUsageArray`  | Yes  | Array of company disk use.  |

## Examples {#section-cb16a97badc94076ad5da277db5ed16a}

The name of this request is misleading. Rather than returning merely a scalar value that reflects how much disk space a company is using, it gets other information about the structure of a company as well.

**Request** 

```java
<ns1:getDiskUsageParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getDiskUsageParam>
```

**Response** 

```java
<getDiskUsageReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <diskUsageArray>
      <items>
         <companyHandle>47</companyHandle>
         <companyName>My Company</companyName>
         <imageCount>207</imageCount>
         <diskSpaceUsage>3024</diskSpaceUsage>
         <lastModified>2007-09-14T22:10:30.661-07:00</lastModified>
      </items>
   </diskUsageArray>
</getDiskUsageReturn>
```

