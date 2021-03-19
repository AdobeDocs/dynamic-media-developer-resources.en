---
description: Sets the list of assets associated with an image set.
seo-description: Sets the list of assets associated with an image set.
seo-title: setImageSetMembers
solution: Experience Manager
title: setImageSetMembers
uuid: 84a73ff4-e93f-4764-80e8-e15f1fec1aeb
feature: "Dynamic Media Classic,SDK/API,Image Sets"
role: "Developer,Administrator"
---

# setImageSetMembers{#setimagesetmembers}

Sets the list of assets associated with an image set.

 This operation ignores the `pageReset` parameter for `ImageSets` and `SpinSets` and forces the value to true. 

## Authorized User Types {#section-8968d6a39a344cfc8521020d92ae8916}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

>[!NOTE]
>
>The user must have read and write access to the image set asset and read access to each member asset.

## Parameters {#section-2f46efcd24c648aeacba738509426e46}

**Input (setImageSetMembersParam)** 

<table id="table_0CBBB65BCEFD4125A4069A080DFC873A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Name </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Required </p> </th> 
   <th colname="col4" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Yes </p> </td> 
   <td colname="col4"> <p>Company handle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> Image set handle. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> memberArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ImageSetMemberUpdateArray</span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> Array of asset members that belong to the image set. </td> 
  </tr> 
 </tbody> 
</table>

**Output (setImageSetMembersReturn)**

The IPS API does not return a response for this operation.

## Examples {#section-7b87219034464aa98524178ccee27738}

This code sample uses a member array to set the members of an image set.

**Request** 

```java
<setImageSetMembersParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>34205|22|929</assetHandle>
   <memberArray>
      <items>
         <assetHandle>24266|1|17062</assetHandle>
         <pageReset>true</pageReset>
      </items>
   </memberArray>
</setImageSetMembersParam>
```

**Response**

None. 
