---
description: Removes folder permissions.
seo-description: Removes folder permissions.
seo-title: removeFolderPermissions
solution: Experience Manager
title: removeFolderPermissions
uuid: cd9f7a42-e314-4ec9-abe2-a27581c7cd23
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Administrator"
---

# removeFolderPermissions{#removefolderpermissions}

Removes folder permissions.

 Syntax 

## Authorized User Types {#section-bfa745624f9b43aaba6c226ac6700fe7}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-7efa68377fd846219b906d354ae64ed3}

**Input (removeFolderPermissionsParam)** 

<table id="table_15223256C63C4F008BDB1DF6F0AFE6A8"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> The handle to the company with folders with permissions you want to remove. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> Handle to the folder. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateChildren</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> <p>When <span class="codeph"> true</span>: 
     <ul id="ul_1305D060E0F34A61AA3C827E43F296E6"> 
      <li id="li_AB8705F3CEAD4B8A8F1C28291A6F7EC8">Permissions removal propagates through all of the folder permission operations. </li> 
     </ul> </p> <p>When <span class="codeph"> false</span>: 
     <ul id="ul_19AEE80F1FC84B64AD623E050C12A0CD"> 
      <li id="li_B8B78851004C43DB8CB7958E380AF510">The operation affects the specified folder only. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (removeFolderPermissionsReturn)**

The IPS API does not return a response for this operation.

## Examples {#section-04390f0ec7cc460cb5d34d518e33e7a5}

This code sample removes permissions from a folder and its sub-folders. Set `updateChildren` to `false` if you need to remove permissions from the parent folder only.

**Request** 

```java
<removeFolderPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <folderHandle>blackmesa/Awatermark/</folderHandle>
   <updateChildren>true</updateChildren>
</removeFolderPermissionsParam>
```

**Response**

None. 
