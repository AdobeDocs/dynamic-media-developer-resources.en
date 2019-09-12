---
description: Update folder permissions.
seo-description: Update folder permissions.
seo-title: updateFolderPermissions
solution: Experience Manager
title: updateFolderPermissions
topic: Scene7 Image Production System API
uuid: 940d7b63-80cf-4097-9cf9-8499b69181b7
index: y
internal: n
snippet: y
---

# updateFolderPermissions{#updatefolderpermissions}

Update folder permissions.

 Syntax 

## Authorized User Types {#section-e5c2217231bf4b3386e0ab3f2e9aca0b}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-339e6e17c5504e1ea79fbdc05f618050}

**Input (updateFolderPermissionsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`companyHandle`*`  | `xsd:string`  | Yes  | Company handle.  |
|  ` *`folderHandle`*`  | `xsd:string`  | Yes  | Folder handle.  |
|  ` *`updateChildren`*`  | `xsd:boolean`  | Yes  | Determines whether to update children with permissions set for the top-level folder.  |
|  ` *`updateArray`*`  | `types:PermissionUpdateArray`  | Yes  | The array of permission updates you want to apply to the folder.  |

**Output (updateFolderPermissionsReturn)**

The IPS API does not return a response for this operation.

## Examples {#section-c3fe4d4388674870a3856c35ef66b631}

**Request** 

```java
<ns1:updateFolderPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/eCatalogs/</ns1:folderHandle>
   <ns1:updateChildren>false</ns1:updateChildren>
   <ns1:updateArray>
      <ns1:items>
         <ns1:groupHandle>225</ns1:groupHandle>
         <ns1:permissionType>Read</ns1:permissionType>
         <ns1:isAllowed>true</ns1:isAllowed>
         <ns1:isOverride>true</ns1:isOverride>
      </ns1:items>
   </ns1:updateArray>
</ns1:updateFolderPermissionsParam>
```

**Response**

None. 
