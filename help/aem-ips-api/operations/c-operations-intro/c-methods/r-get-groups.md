---
description: Returns company groups.
solution: Experience Manager
title: getGroups
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d98c08a6-4c20-4538-9598-c905078ab7de
TQID: https://experienceleague.adobe.com/Y2l5-bdc18NlkUFnKw3-cCAF--62ORuYyXaTlsUZ8uE
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# getGroups{#getgroups}

Returns company groups.

 Syntax 

## Authorized User Types {#section-27c77680a2f34e2f9ecd0af4ebb6847e}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-0e06195f23dd4c69922df210f566dd18}

**Input (getGroupsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | The handle to the company.  |

**Output (getGroupsReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  groupArray  | `types:GroupArray`  | Yes  | Array of groups.  |

## Examples {#section-ed0708f611574354bf0c6ea83912b531}

This code returns an array that contains all the groups that belong to a specific company and specific information about each group.

**Request** 

```java
<ns1:getGroupsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getGroupsParam>
```

```java
<getGroupsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupArray>
      <items>
         <groupHandle>225</groupHandle>
         <companyHandle>47</companyHandle>
         <name>MyGroup</name>
         <isSystemDefined>false</isSystemDefined>
      </items>
   </groupArray>
</getGroupsReturn>
```
