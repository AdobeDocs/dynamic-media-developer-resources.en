---
description: Deletes a folder.
solution: Experience Manager
title: deleteFolder
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c042b87b-3f60-4608-8ed5-0fc031a66c03
---
# deleteFolder{#deletefolder}

Deletes a folder.

 Syntax 

## Authorized User Types {#section-1c15a74c41194744a81f5ca86fe26585}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

>[!NOTE]
>
>The user must have read and delete access to the folder and all of its children.

## Parameters {#section-a793c98a481a4f26ab50bc69b16b57e7}

**Input (deleteFolderParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company to which the folder belongs.  |
|  `*`folderHandle`*`  | `xsd:string`  | Yes  | The handle to the folder to delete.  |

**Output (deleteFolderParam)**

The IPS API does not return a response for this operation.

## Examples {#section-9d4617b322e8442d80e59be0f8714841}

This sample code deletes a folder from the root of the company. It requires a folder handle, which you must obtain from another operation.

**Request** 

```java
<ns1:deleteFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/SpinSets/</ns1:folderHandle>
</ns1:deleteFolderParam>
```

None.
