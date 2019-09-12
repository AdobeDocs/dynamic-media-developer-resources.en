---
description: Returns the members of a group.
seo-description: Returns the members of a group.
seo-title: getGroupMembership
solution: Experience Manager
title: getGroupMembership
topic: Scene7 Image Production System API
uuid: 5ec48e8c-378b-43a3-b3dc-aa21dbf339b5
index: y
internal: n
snippet: y
---

# getGroupMembership{#getgroupmembership}

Returns the members of a group.

 Syntax 

## Authorized User Types {#section-35d070e5c4d74ca69df508368953cfb8}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-2e92f850254e46e48403acaa215341a5}

**Input (getGroupMembershipParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`userHandle`*`  | `xsd:string`  | No  | The handle to the user.  |
|  ` *`companyHandle`*`  | `xsd:string`  | No  | The handle to the company.  |

**Output (getGroupMembershipReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`groupArray`*`  | `types:GroupArray`  | Yes  | Array of groups.  |

## Examples {#section-ebb437369f4f4487b3eb2ef0c078b8ae}

This code sample returns all the members of a group. Because the company and user handles are optional, the operation can return all members of all groups.

**Request** 

```java
<ns1:getGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getGroupMembershipParam>
```

**Response** 

```java
<getGroupMembershipReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupArray>
      <items>
         <groupHandle>225</groupHandle><companyHandle>47</companyHandle><name>MyGroup</name><isSystemDefined>false</isSystemDefined></items></groupArray></getGroupMembershipReturn>
```

