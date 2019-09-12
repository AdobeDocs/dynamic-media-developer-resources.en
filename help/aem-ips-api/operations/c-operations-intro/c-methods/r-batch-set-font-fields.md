---
description: Sets font metadata fields.
seo-description: Sets font metadata fields.
seo-title: batchSetFontFields
solution: Experience Manager
title: batchSetFontFields
topic: Scene7 Image Production System API
uuid: 0209865e-32b3-4bea-a508-05771a0365e1
index: y
internal: n
snippet: y
---

# batchSetFontFields{#batchsetfontfields}

Sets font metadata fields.

## Authorized User Types {#section-89eff13b5ed54cddb87b1304ba4eff0e}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-836f5948d00a46e98ccb62f0573e4e68}

**Input (batchSetFontFieldsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`companyHandle`*`  | `xsd:string`  | Yes  | Handle to the company that contains the fonts.  |
|  ` *`updateArray`*`  | `types:FontFieldUpdateArray`  | Yes  | Array of font field updates.  |

**Output (batchSetFontFieldsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`successCount`*`  | `xsd:int`  | Yes  | The number of successfully set font fields.  |
|  ` *`warningCount`*`  | `xsd:int`  | Yes  | Number of warnings generated when the operation attempted to set font fields.  |
|  ` *`errorCount`*`  | `xsd:int`  | Yes  | Number of errors generated when the operation attempted to set font fields.  |
|  ` *`warningDetailArray`*`  | `types:AssetOperationFaultArray`  | No  | The array of details associated with the assets that generated warnings when the operation attempted to apply the updates.  |
|  ` *`errorDetailArray`*`  | `types:AssetOperationFaultArray`  | No  | The array of details associated with the assets that generated errors when the operation attempted to apply the updates.  |

## Examples {#section-0449c2e4ec534f4b8ee849ec4fe12c4e}

**Request** 

```java
<batchSetFontFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
   <updateArray>
      <items>
          <assetHandle>a|450|14|19</assetHandle>
          <fontName>Bookman Old Style Font Name</fontName>
          <postscriptName>Bookman Old Style PostScript</postscriptName>
          <rtfName>Bookman Old Style RTF</rtfName>
          <fontFamily>Bookman Old Style Family</fontFamily>
          <style>BoldItalic</style>
          <typeName>Open Type</typeName><type>OTF</type>
      </items>
   </updateArray>
</batchSetFontFieldsParam>
```

**Response** 

```java
<batchSetFontFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetFontFieldsReturn>
```

