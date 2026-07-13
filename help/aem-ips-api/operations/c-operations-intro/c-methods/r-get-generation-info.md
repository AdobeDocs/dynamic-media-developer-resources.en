---
description: Returns 2 different types of information based on the parameters passed in. originatorHandle returns information about assets generated from the specified asset. generateHandle returns information about steps used to generate the specified asset or file.
solution: Experience Manager
title: getGenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa098e3c-8145-4238-a84c-c545f1c53341
TQID: 'https://experienceleague.adobe.com/MA0SJinQzPjDFkSXVRhH2e7A3Ry6HXoW--K-elv028M'
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
# getGenerationInfo{#getgenerationinfo}

Returns 2 different types of information based on the parameters passed in. originatorHandle returns information about assets generated from the specified asset. generateHandle returns information about steps used to generate the specified asset or file.

 Syntax 

## Authorized User Types {#section-9cc2216b32c74107be07aeacecc11401}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `TrialSiteUser` 
* `ImagePortalAdmin` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-b7fa94c82147455888e8469fa5f6922b}

**Input (getGenerationInfoParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  Code Phrase  | `xsd:string`  | Yes  | The handle to the company.  |
|  Code Phrase  | `xsd:string`  | No  | The engine that was used in the generation. See Font Styles.  |
|  Code Phrase  | `xsd:string`  | No  | The handle of the asset to query for generated assets.  |
|  Code Phrase  | `xsd:string`  | No  | The handle of the asset to query for assets and engines used in its generation.  |
|  Code Phrase  | `xsd:StringArray`  | No  | Properties included in the operation.  |
|  Code Phrase  | `xsd:StringArray`  | No  | Properties excluded from the operation.  |

**Output (getGenerationInfoReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  generationArray  | `types:GenerationInfoArray`  | Yes  | Array of generation information.  |

## Examples {#section-fdffe6ed82d94c7aa90e47f7ce889403}

This code sample returns information about assets generated from a specific asset. It does not retrieve information about steps used to generate the specified asset. The response is truncated for brevity.

**Request** 

```java
<getGenerationInfoParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <originatorHandle>a|716|25|160</originatorHandle>
</getGenerationInfoParam>
```

**Response** 

```java
<getGenerationInfoReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <generationArray>
      <items>
         <engine>PostScriptRip</engine>
         <originator>
         ...
         </generated>
         <attributeArray/>
      </items>
   </generationArray>
</getGenerationInfoReturn>
```

