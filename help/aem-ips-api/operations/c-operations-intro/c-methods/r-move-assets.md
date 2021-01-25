---
description: Moves multiple assets independently of each other. It accomplishes this using the AssetMove type contained in the assetMoveArray. Each AssetMove field contains a destination folder.
seo-description: Moves multiple assets independently of each other. It accomplishes this using the AssetMove type contained in the assetMoveArray. Each AssetMove field contains a destination folder.
seo-title: moveAssets
solution: Experience Manager
title: moveAssets
topic: Dynamic Media Image Production System API
uuid: 178f9979-fff5-45ce-a001-1263d1770ea8
---

# moveAssets{#moveassets}

Moves multiple assets independently of each other. It accomplishes this using the AssetMove type contained in the assetMoveArray. Each AssetMove field contains a destination folder.

 Syntax 

## Authorized User Types {#section-4166515fd9d8487b8af37465ce61802b}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-7d47f663474b41cc83439288ac133cc5}

**Input (moveAssetsReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company with assets to be moved.  |
|  `*`assetMoveArray`*`  | `types:AssetMoveArray`  | Yes  | An asset move array. It contains an asset and an asset destination folder.  |

**Output (moveAssetsReturn)** 

<table id="table_FD902FAB4F98413C8A051270ADD7D9C7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Required </th> 
   <th colname="col4" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> successCount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> Successfully moved asset count. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningCount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> Count of assets that generated warnings when the operation attempted to move them. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorCount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> Count of assets that generated errors when the operation attempted to move them. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningDetailArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:AssetOperationFaultArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <span class="codeph"> AssetOperationFaults</span>that contain the: 
    <ul id="ul_689F4A87A68140F18DFB43868226A409"> 
     <li id="li_274C8BF5932F4AF584AA92F25E0F33C6">Assets that threw the warnings. </li> 
     <li id="li_5CC4A9120CA94F968CAF0D0135C49E0A">Warning codes. </li> 
     <li id="li_AEC91FA68B2E43BC8BAA108C743F5667">Reason for the warning. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorDetailArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:AssetOperationFaultArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <span class="codeph"> AssetOperationFaults</span>that contain the: 
    <ul id="ul_C397BC384A134F429D01ADA28DF2E097"> 
     <li id="li_EAEBB5F539164480BA9EAA7C8FFBF69A">Assets that threw the errors. </li> 
     <li id="li_F96D5FBB2F7A402AA36D8DFA3971391D">Error codes. </li> 
     <li id="li_F610415E416F43DDA4B1DBF1897E2F61">Reason for the errors. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Examples {#section-c31ed4c004ab4b3fa42c96d26ceb5ce7}

This code sample moves assets to a specific location specified by the `assetMoveArray`. The array includes the asset handle and its folder handle. The response indicates the assets were moved successfully.

**Request** 

```java
<moveAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetMoveArray>
      <items>
          <assetHandle>a|942|1|579</assetHandle>
          <folderHandle>ApiTestCo/uploads/</folderHandle>
      </items>
      <items>
         <assetHandle>a|943|1|580</assetHandle>
         <folderHandle>ApiTestCo/uploads/</folderHandle>
      </items>
   </assetMoveArray>
</moveAssetsParam>
```

**Response** 

```java
<moveAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</moveAssetsReturn>
```

