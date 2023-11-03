---
description: Returns all folders and subfolders, starting at the folder path. The getFolders response returns a maximum of 100,000 folders.
solution: Experience Manager
title: getFolders
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 71fe3343-2560-4d74-8ec3-1229d83a62e1
---
# getFolders{#getfolders}

Returns all folders and subfolders, starting at the folder path. The getFolders response returns a maximum of 100,000 folders.

## Purpose of Folders {#section-66e344d5333f42f1b060a0cba25935c3}

A folder enables you to organize subfolders and assets. All folder and asset names must be unique. Folders and assets that share the same name cause a namespace conflict, even if they are in different folder hierarchies. 
Syntax 

## Authorized User Types {#section-0dc7e17cb60f4cf7bcdb76648e5d2f8e}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `TrialSiteUser` 
* `ImagePortalAdmin` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

>[!NOTE]
>
>The user must have read access to the folder to return data on it.

## Parameters {#section-0c1976503eaa418a9226b51667901176}

**Input (getFoldersParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | The handle to the company.  |
|  accessUserHandle  | `xsd:string`  | No  | Used by administrators to impersonate a specific user.  |
|  accessGroupHandle  | `xsd:string`  | No  | Filter by a specific group.  |
|  folderPath  | `xsd:string`  | No  | The root folder to retrieve folders and all subfolders to the leaf level. If excluded, the company root is used.  |
|  assetTypeArray  | `types:StringArray`  | No  | Returns folders that only contain specified asset types.  |
|  responseFieldArray  | `types:StringArray`  | No  | Contains a list of fields that you want to include in the response.  |
|  excludeFieldArray  | `types:StringArray`  | No  | Contains a list of fields you want to exclude from the response.  |

**Output (getFoldersReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  folderArray  | `types:FolderArray`  | No  | An array of folders that match the filter criteria. The response is limited to 100,000 folders maximum.  |
|  permissionsSetArray  | `types:PermissionSetArray`  |  |  |

## Examples {#section-b5cb06e9fb9945ad898dbdc3692b754e}

This code sample returns an array that contains all the folders for a company along with specific information about each folder.

**Request** 

```java
<ns1:getFoldersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getFoldersParam>
```

**Response** 

```java
<getFoldersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <folderArray>
      <items>
         <folderHandle>MyCompany/</folderHandle>
         <path>MyCompany/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
      <items>
         <folderHandle>MyCompany/eCatalogs/</folderHandle>
         <path>MyCompany/eCatalogs/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
      <items>
         <folderHandle>MyCompany/PDF/</folderHandle>
         <path>MyCompany/PDF/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
   </folderArray>
</getFoldersReturn>
```
