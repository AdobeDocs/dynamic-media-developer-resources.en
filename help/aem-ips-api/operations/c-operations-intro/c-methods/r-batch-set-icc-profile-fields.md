---
description: Sets ICC profile metadata fields.
solution: Experience Manager
title: batchSetIccProfileFields
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d10a30ca-afa7-4ef0-8cef-0329b0068bf3
TQID: https://experienceleague.adobe.com/o-JFv3qFz4d9C-ICXtwv3L3VUg7hotgwUfR-oscL6Lg
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
# batchSetIccProfileFields{#batchseticcprofilefields}

Sets ICC profile metadata fields.

 Syntax 

## Authorized User Types {#section-f6f7caf9434b4f469518dab64b76c0f4}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-75a02b55ae0d444ca26b59aac6e86d6f}

**Input (batchSetIccProfileFields)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | Handle to the company that contains the ICC profiles.  |
|  update array  | `xsd:string`  | Yes  | Array of ICC profile updates.  |

**Output (batchSetIccProfileFields)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  successCount  | `xsd:int`  | Yes  | The number of successfully set ICC profile fields.  |
|  warningCount  | `xsd:int`  | Yes  | The number of warnings generated when the operation attempted to set the ICC profile fields.  |
|  errorCount  | `xsd:int`  | Yes  | The number of errors generated when the operation attempted to set the ICC profile fields.  |
|  warningDetailArray  | `types:AssetOperationFaultArray`  | No  | The array of details associated with the assets that generated warnings when the operation attempted to apply the updates.  |
|  errorDetailArray  | `types:AssetOperationFaultArray`  | No  | The array of details associated with the assets that generated errors when the operation attempted to apply the updates.  |

## Examples {#section-5dc90cfbd9b1411485b44859032f7cb9}

**Request** 

```java {.line-numbers}
<batchSetIccProfileFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|1808|13|169</assetHandle>
         <class>Output</class>
         <colorSpace>CMYK</colorSpace>
         <pcsType>Luv</pcsType>
      </items>
   </updateArray>
</batchSetIccProfileFieldsParam>
```

**Response** 

```java {.line-numbers}
<batchSetIccProfileFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetIccProfileFieldsReturn>
```
