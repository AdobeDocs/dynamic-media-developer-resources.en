---
description: Returns all values for a metadata field.
solution: Experience Manager
title: getDistinctMetadataValues
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Administrator
---

# getDistinctMetadataValues{#getdistinctmetadatavalues}

Returns all values for a metadata field.

 Syntax 

## Authorized User Types {#section-f0f44fdcb318490582dd04de8eaf745d}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-600f36a32ff147cb83149943d37843e2}

**Input (getDistinctMetadataValuesParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company that you want to get data for.  |
|  `*`metadataKey`*`  | `xsd:string`  | Yes  | Metadata key in dot notation.  |

**Output (getDistinctMetadataValuesReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`valueArray`*`  | `types:ValueArray`  | Yes  | Values of the requested metadata field.  |

## Examples {#section-0189fa6fb31646cda5ce1b0bc4fcdf46}

**Request** 

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:xsd="http://www.scene7.com/IpsApi/xsd"
xmlns:ns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <soapenv:Header>
      <xsd:authHeader>
         <xsd:user>user@company.com</xsd:user>
         <xsd:password>password</xsd:password>
      </xsd:authHeader>
   </soapenv:Header>
   <soapenv:Body>
   <ns:getDistinctMetadataValuesParam>
      <ns:companyHandle>680</ns:companyHandle>
      <ns:metadataKey>dc.format</ns:metadataKey>
      </ns:getDistinctMetadataValuesParam>
   </soapenv:Body>
</soapenv:Envelope>
```

**Response** 

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/">
   <soapenv:Body>
      <getDistinctMetadataValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
         <valueArray>
            <items>
               <value>N/A</value>
               <count>412</count>
            </items>
            <items>
               <value>image/jpeg</value>
               <count>189</count>
            </items>
            <items>
               <value>image/epsf</value>
               <count>1</count>
            </items>
            <items>
               <value>image/tiff</value>
               <count>3</count>
            </items>
         </valueArray>
      </getDistinctMetadataValuesReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

