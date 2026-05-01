---
description: Deletes a zoom target.
solution: Experience Manager
title: deleteZoomTarget
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa1f7cf8-038a-4fa8-b869-12ce4b2ad41f
TQID: https://experienceleague.adobe.com/9YbRelPNGO-62AFmg18k2QlksE0MdTQboYN9-AaS6LQ
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# deleteZoomTarget{#deletezoomtarget}

Deletes a zoom target.

## Authorized User Types {#section-09ca82bc817e49048271c5cba545702e}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

>[!NOTE]
>
>The user must have read and write access to the asset.

## Parameters {#section-225330a45e7a408f8375e084677d9cb1}

**Input (deleteZoomTargetParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | The handle to the company to which the zoom target belongs.  |
|  zoomTargetHandle  | `xsd:string`  | Yes  | The handle to the zoom target to delete.  |

**Output (deleteZoomTargetParam)**

The IPS API does not return a response for this operation.

## Example {#section-a35857a5ca884357a879f7ba6cf985fe}

This code sample deletes a zoom target from a company.

**Request** 

```java
<ns1:deleteZoomTargetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:zoomTargetHandle>34194|9|301</ns1:zoomTargetHandle>
</ns1:deleteZoomTargetParam>
```

**Response**

None.
