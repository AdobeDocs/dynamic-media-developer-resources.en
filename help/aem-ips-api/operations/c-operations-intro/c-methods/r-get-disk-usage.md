---
description: Returns information about a company's structure (number of files, and so on.).
solution: Experience Manager
title: getDiskUsage
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 06fdd9f5-5021-4f0b-b312-4465df9bda25
TQID: 'https://experienceleague.adobe.com/mF0YHIw8BZhBRK240EmiiaHoyBbTdaW-ajl7veY1ywk'
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
---
# getDiskUsage{#getdiskusage}

Returns information about a company's structure (number of files, and so on.).

## Authorized User Types {#authorized-user-types}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-e7e47082faf44ae28a2cfa7ef53aedbb}

**Input (getDiskUsageParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | The handle to the company whose disk usage you want to obtain.  |

**Output (getDiskUsageReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  diskUsageArray  | `types:DiskUsageArray`  | Yes  | Array of company disk use.  |

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

