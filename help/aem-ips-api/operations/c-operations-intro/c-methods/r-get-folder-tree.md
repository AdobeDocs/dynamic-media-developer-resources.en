---
description: Returns folders and subfolders in a hierarchical tree structure. The getFolderTree response is limited to a maximum of 100,000 folders
solution: Experience Manager
title: getFolderTree
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
---

# getFolderTree{#getfoldertree}

Returns folders and subfolders in a hierarchical tree structure. The getFolderTree response is limited to a maximum of 100,000 folders

 Syntax 

## Authorized User Types {#section-66ef19149f4d4123a3a99004b5a2743e}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `TrialSiteUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

>[!NOTE]
>
>The user must have read access to the folder to return data on it.

## Parameters {#section-0c2b30513f1e439cbd840e8cc6465b3a}

**Input (getFolderTreeParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company.  |
|  `*`accessUserHandle`*`  | `xsd:string`  | No  | Used only by administrators to impersonate a specific user.  |
|  `*`accessGroupHandle`*`  | `xsd:string`  | No  | Used to filter by a specific group, including any of those to which the company belongs.  |
|  `*`folderPath`*`  | `xsd:string`  | No  | The root folder to retrieve folders and all subfolders to the leaf level. If excluded, the company root is used.  |
|  `*`depth`*`  | `xsd:int`  | Yes  | A value of zero gets the top-level folder. Any other value specifies the depth to descend into the tree.  |
|  `*`assetTypeArray`*`  | `types:StringArray`  | No  | Returns folders that only contain specified asset types.  |
|  `*`responseFieldArray`*`  | `types:StringArray`  | No  | Contains a list of fields that you want to include in the response.  |
|  `*`excludeFieldArray`*`  | `types:StringArray`  | No  | Contains a list of fields that you want to exclude in the response.  |

**Output (getFolderTreeReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`folders`*`  | `types:folders`  | No  | The hierarchy of folders in a tree structure. The response is limited to a maximum of 100,000 folders.  |
|  `*`permissionSetArray`*`  | `types:PermissionSetArray`  |  |  |

## Examples {#section-a9fd2edb56574dd9bf8b0f2fd89367e4}

This code sample uses a company handle and a depth parameter to determine the level of depth the response should return. The response contains folders and subfolder arrays with related. Set the depth value to a smaller number to search deeper into the folder tree.

**Request** 

```java
<ns1:getFolderTreeParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:depth>-1</ns1:depth>
</ns1:getFolderTreeParam>
```

**Response**

```java

<getFolderTreeReturn xmlns="http://www.scene7.com/IpsApi/xsd/">
  <folders>
    <items>
      <folderHandle>f|sampleFolder/uploadTestDir/</folderHandle>
      <path>MyCompany/uploadTestDir/</path>
      <lastModified>2011-11-14T11:19:59.031-08:00</lastModified>
      <childLastModified>2011-11-14T11:19:59.031-08:00</childLastModified>
      <permissionSetHandle>pm|2</permissionSetHandle>
      <hasSubfolders>true</hasSubfolders>
      <subfolderArray>
        <items>
          <folderHandle>f|MyCompany/uploadTestDir/SubFolder/</folderHandle>
          <path>DevanCo/uploadTestDir/SubFolder/</path>
          <lastModified>2011-11-14T11:19:59.032-08:00</lastModified>
          <childLastModified>2011-11-14T11:19:59.032-08:00</childLastModified>
          <permissionSetHandle>pm|2</permissionSetHandle>
          <hasSubfolders>true</hasSubfolders>
          <subfolderArray>
            <items>
              <folderHandle>f|MyCompany/uploadTestDir/SubFolder/10/</folderHandle>
              <path>DevanCo/uploadTestDir/SubFolder/10/</path>
              <lastModified>2011-11-14T11:19:59.033-08:00</lastModified>
              <childLastModified>2011-11-14T15:06:58.563-08:00</childLastModified>
              <permissionSetHandle>pm|2</permissionSetHandle>
              <hasSubfolders>false</hasSubfolders>
            </items>
          </subfolderArray>
        </items>
      </subfolderArray>
    </items>
  </folders>
  <permissionSetArray>
    <items>
      <permissionSetHandle>pm|2</permissionSetHandle>
      <permissionArray>
        <items>
          <groupHandle>g|1</groupHandle>
          <groupName>Asset Download Group</groupName>
          <permissionType>Read</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>false</isOverride>
        </items>
        <items>
          <groupHandle>g|2</groupHandle>
          <groupName>Asset Upload Group</groupName>
          <permissionType>Read</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>true</isOverride>
        </items>
        <items>
          <groupHandle>g|2</groupHandle>
          <groupName>Asset Upload Group</groupName>
          <permissionType>Write</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>true</isOverride>
        </items>
      </permissionArray>
    </items>
  <permissionSetArray>
</getFolderTreeReturn>

```

