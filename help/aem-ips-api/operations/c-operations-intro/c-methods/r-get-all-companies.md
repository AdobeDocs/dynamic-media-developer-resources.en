---
description: Returns an array of all companies.
solution: Experience Manager
title: getAllCompanies
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0e339ecf-83b5-410c-8683-f3d73bd92339
TQID: 'https://experienceleague.adobe.com/B2wkv6Xvuvg17yqUucjIx170K4YmznQgBrJiVgLe2qg'
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
# getAllCompanies{#getallcompanies}

Returns an array of all companies.

 Syntax 

## Authorized User Types {#section-773db3753b4842e5a4623ad810176508}

* `IpsAdmin`

## Parameters {#section-efd74992e6904ebabe7383b577af4fdb}

**Input (getAllCompaniesParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  includeExpired  | `xsd:boolean`  | Yes  | Set to true to return expired and non-expired companies.  |

**Output (getAllCompaniesReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyArray  | `types:CompanyArray`  | Yes  | The array of companies.  |

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

