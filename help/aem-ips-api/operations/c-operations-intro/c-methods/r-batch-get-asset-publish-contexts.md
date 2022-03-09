---
description: Returns the publish contexts for assets marked for publication.
solution: Experience Manager
title: batchGetAssetPublishContexts
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: ba1f62a7-2698-4300-b6de-6d07ac764b0c
---
# batchGetAssetPublishContexts{#batchgetassetpublishcontexts}

Returns the publish contexts for assets marked for publication.

 Syntax 

## Authorized User Types {#section-d5362ca8a6ab42949cd648ba38dbf2f8}

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

## Parameters {#section-1742fcb196224545b270eb8241f757a8}

**Input (batchGetAssetPublishContextsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | Handle to the company.  |
|  assetHandleArray  | ` `types:HandleArray``  | Yes  | A list of assets you want to query for active (marked for publish) contexts.  |

**Output (batchGetAssetPublishContextsReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  assetPublishContextsArray  | `types:assetPublishContextsArray`  | Yes  | An array of publish contexts in which each asset is marked for publish.  |

## Examples {#section-457f6809ccfa425b9a0976313d613f4e}

**Request** 

```java {.line-numbers}
<batchGetAssetPublishContextsParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
  <assetHandleArray>
    <items>a|27007</items>
    <items>a|27008</items>
  </assetHandleArray>
</batchGetAssetPublishContextsParam>
```

**Response** 

```java {.line-numbers}
<batchGetAssetPublishContextsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <assetPublishContextsArray>
    <items>
      <assetHandle>a|27007</assetHandle>
      <publishContextArray>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <contextName>ImageServing</contextName>
          <contextType>ImageServing</contextType>
        </items>
      </publishContextArray>
    </items>
    <items>
      <assetHandle>a|27008</assetHandle>
      <publishContextArray>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <contextName>Video</contextName>
          <contextType>Video</contextType>
        </items>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <contextName>ImageRendering</contextName>
          <contextType>ImageRendering</contextType>
        </items>
      </publishContextArray>
    </items>
  </assetPublishContextsArray>
</batchGetAssetPublishContextsReturn>
```
