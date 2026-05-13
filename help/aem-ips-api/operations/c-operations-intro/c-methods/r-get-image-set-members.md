---
description: Gets an array of members that are in an image set.
solution: Experience Manager
title: getImageSetMembers
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 29ceef8b-127f-4460-8623-c3e26c959327
TQID: 'https://experienceleague.adobe.com/7tS3wEIqaBPmykuVmDBfq9GugDcbnevj-XAQQHM3icY'
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
# getImageSetMembers{#getimagesetmembers}

Gets an array of members that are in an image set.

 Syntax 

## Authorized User Types {#section-eaa3a167fa77403ea1b374b05fff4ded}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `TrialSiteUser` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

>[!NOTE]
>
>Requires read access to the image and member set asset.

## Parameters {#section-a67ba98095574533980997c83ceaa316}

**Input (getImageSetMembersParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | The handle to the company that contains the image set.  |
|  assetHandle  | `xsd:string`  | Yes  | The image set asset handle.  |

**Output (getImageSetMembersReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  memberArray  | `types:ImageSetMemberArray`  | No  | Array of image set members.  |

## Examples {#section-888a9a78033346f39b171229de93dfa0}

This code sample returns specific image set members. The response returns an empty array.

**Request** 

```java
<ns1:getImageSetMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>34195|22|927</ns1:assetHandle>
</ns1:getImageSetMembersParam>
```

**Response** 

```java
<getImageSetMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <memberArray></memberArray>
</getImageSetMembersReturn>
```
