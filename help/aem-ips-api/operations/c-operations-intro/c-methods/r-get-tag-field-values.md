---
description: Gets all tag dictionary values defined for one or more tag fields.
seo-description: Gets all tag dictionary values defined for one or more tag fields.
seo-title: getTagFieldValues
solution: Experience Manager
title: getTagFieldValues
uuid: 92d84dfc-6a6c-4876-9670-1152adb6317c
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
---

# getTagFieldValues{#gettagfieldvalues}

Gets all tag dictionary values defined for one or more tag fields.

 Syntax 

## Authorized User Types {#section-cc36a437394c491594e704a08a161c87}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `TrialSiteUser` 
* `ImagePortalAdmin` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-9ad806e7736e4d51ae42cad185050cf9}

**Input (getTagFieldValuesReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | The handle of the company containing the tag field.  |
|  `*`fieldHandleArray`*`  | `types:HandleArray`  | Yes  | An array of field handles to tag values you want returned.  |

**Output (getTagFieldValuesReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`fieldArray`*`  | `types:TagFieldValuesArray`  | Yes  | An array of the tag values in the dictionary for each requested field.  |

## Examples {#section-4492742614e44bb191a7d397dc1a1407}

**Request** 

```java
<getTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandleArray>
      <items>m|3|ASSET|SingleOpenTag</items>
      <items>m|3|ASSET|SingleFixedTag</items>
   </fieldHandleArray>
</getTagFieldValuesParam>
```

**Response** 

```java
<getTagFieldValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <fieldArray>
      <items>
         <fieldHandle>m|3|ASSET|SingleOpenTag</fieldHandle>
         <valueArray>
            <items>GroupB</items>
            <items>GroupA</items>
         </valueArray>
      </items>
      <items>
         <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
         <valueArray>
            <items>North</items>
            <items>South</items>
            <items>East</items><items>West</items>
         </valueArray>
      </items>
   </fieldArray>
</getTagFieldValuesReturn>
```

