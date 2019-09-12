---
description: Returns an array of all companies.
seo-description: Returns an array of all companies.
seo-title: getAllCompanies
solution: Experience Manager
title: getAllCompanies
topic: Scene7 Image Production System API
uuid: bc2d82b1-e020-4dfe-9704-601ef5aa2111
index: y
internal: n
snippet: y
---

# getAllCompanies{#getallcompanies}

Returns an array of all companies.

 Syntax 

## Authorized User Types {#section-773db3753b4842e5a4623ad810176508}

* `IpsAdmin`

## Parameters {#section-efd74992e6904ebabe7383b577af4fdb}

**Input (getAllCompaniesParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`includeExpired`*`  | `xsd:boolean`  | Yes  | Set to true to return expired and non-expired companies.  |

**Output (getAllCompaniesReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`companyArray`*`  | `types:CompanyArray`  | Yes  | The array of companies.  |

## Examples {#section-3eecf4e6900b41fb92a0e3214791c6b9}

This code sample returns all companies in IPS in an array. Note, the sample response is truncated for brevity.

**Request** 

```java
<ns1:getAllCompaniesParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:includeExpired>false</ns1:includeExpired>
</ns1:getAllCompaniesParam>
```

**Response** 

```java
<ns1:getAllCompaniesReturnxmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyArray>
      <ns1:items>
         <ns1:companyHandle>18</ns1:companyHandle>
         <ns1:name>00webload</ns1:name>
         <ns1:rootPath>00webload/</ns1:rootPath>
         <ns1:expires>2101-02-01T07:00:00.667Z</ns1:expires>
      </ns1:items>
      <ns1:items>
         <ns1:companyHandle>19</ns1:companyHandle>
         <ns1:name>01webload</ns1:name>
         <ns1:rootPath>01webload/</ns1:rootPath>
         <ns1:expires>2101-02-01T07:00:00.414Z</ns1:expires>
      </ns1:items>
      . . .
   </ns1:companyArray>
</ns1:getAllCompaniesReturn>
```

