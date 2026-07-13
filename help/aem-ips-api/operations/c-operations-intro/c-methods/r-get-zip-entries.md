---
description: Returns Zip file data.
solution: Experience Manager
title: getZipEntries
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: eb052685-b750-4a12-b00e-28e676340e98
TQID: 'https://experienceleague.adobe.com/-fb25TjtmLMUiZe8gRLz7QmtajqVKASUwwc6TQfjN48'
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
# getZipEntries{#getzipentries}

Returns Zip file data.

 Syntax 

## Authorized User Types {#section-33a3f03ba8a14086922397619ce12ab8}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `TrialSiteUser` 
* `ImagePortalAdmin` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-aa3f498fe76d4a5f99c42d64520fadce}

**Input (getZipEntriesParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | The handle to the company that contains the Zip file.  |
|  assetHandle  | `xsd:string`  | Yes  | Handle to the Zip file.  |

**Output (getZipEntriesReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  zipArray  | `types:ZipEntryArray`  | Yes  | Array of entries in a Zip file.  |

## Examples {#section-1fc0ad8fa448492cb5a135d3e3d161ac}

This code sample returns Zip file information, including compressed and uncompressed size.

**Request** 

```java
<getZipEntriesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetHandle>a|94223|27|30602</assetHandle>
</getZipEntriesParam>
```

**Response** 

```java
<getZipEntriesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <zipArray
      <items>
         <name>Checklist_Images/.DS_Store</name>
         <isDirectory>false</isDirectory>
         <lastModified>2007-05-09T15:41:52.000-07:00</lastModified>
         <compressedSize>503</compressedSize>
         <uncompressedSize>6148</uncompressedSize>
      </items>
   ...
   </zipArray>
</getZipEntriesReturn>
```

