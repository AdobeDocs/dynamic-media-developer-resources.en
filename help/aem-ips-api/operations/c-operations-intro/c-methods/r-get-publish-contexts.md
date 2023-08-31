---
title: getPublishContexts
description: getPublishContexts
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7b26e659-71b9-40c4-9df4-94e78c3e4baf
---
# getPublishContexts{#getpublishcontexts}

 Syntax 

## Authorized User Types {#section-1a3a50349b5640dd8e498ff9e9c37340}

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
>* The user must have read access to return the assets. 
>* All users have access to the shared company. 
>

## Parameters {#section-d08e2175d3f84774b55b91bc590b8b3f}

**Input (getPublishContextsParam)** 

<table id="table_4A505A067586464B99F8F68E3B1BE75E"> 
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
   <td colname="col4"> Handle to the company. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> contextType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4">The type of publishing context that you want to return. Includes: 
    <ul id="ul_21EDF8F0026E402EAE8226A0CADEE652">
     <li id="li_06DB502952D943198F16C06C59816268"><span class="codeph"> ImageServing</span></li>
     <li id="li_E67A42934E8F4689A148CE125F7372AE"><span class="codeph"> ImageRendering</span></li>
     <li id="li_3CB3A9C4E7AB4A71819567A9566E396C"><span class="codeph"> Video</span></li>
     <li id="li_27E3DB89B53B4B50B2231622A157A228"><span class="codeph"> ServerDirectory</span></li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>

**Output (getPublishContextsReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  publishContextArray  | types:PublishContextArray  | Yes  | An array of publish contexts for a company, filtered by context type if necessary.  |

## Examples {#section-23fb7d6a15004b7eb4c3d3bcb37ceb04}

**Request** 

```java
<getPublishContextsParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
</getPublishContextsParam>
```

**Response** 

```java
<getPublishContextsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
  <publishContextArray>
    <items>
      <contextHandle>pc|3001</contextHandle>
      <contextName>ImageRendering</contextName>
      <contextType>ImageRendering</contextType>
    </items>
    <items>
      <contextHandle>pc|3002</contextHandle>
      <contextName>ImageServing</contextName>
      <contextType>ImageServing</contextType>
    </items>
    <items>
      <contextHandle>pc|3003</contextHandle>
      <contextName>ServerDirectory</contextName>
      <contextType>ServerDirectory</contextType>
    </items>
    <items>
      <contextHandle>pc|3004</contextHandle>
      <contextName>Video</contextName>
      <contextType>Video</contextType>
    </items>
  </publishContextArray>
</getPublishContextsReturn>
```
