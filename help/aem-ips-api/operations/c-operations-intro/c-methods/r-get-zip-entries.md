---
description: Returns Zip file data.
solution: Experience Manager
title: getZipEntries
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
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
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company that contains the Zip file.  |
|  `*`assetHandle`*`  | `xsd:string`  | Yes  | Handle to the Zip file.  |

**Output (getZipEntriesReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`zipArray`*`  | `types:ZipEntryArray`  | Yes  | Array of entries in a Zip file.  |

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

