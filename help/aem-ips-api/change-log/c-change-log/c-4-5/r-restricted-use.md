---
description: These new or modified operations and data types available in the beta WSDL are not to be used outside of Dynamic Media developed applications.
solution: Experience Manager
title: Restricted Use
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6602c5bc-9f75-4885-ae14-cab14e6afa5e
---
# Restricted Use{#restricted-use}

These new or modified operations and data types available in the beta WSDL are not to be used outside of Dynamic Media developed applications.

These operations and types are subject to disabling, change or deprecation with subsequent system updates.

**New Types**

* AssetPublishContexts 
* AssetPublishContextsArray 
* CompanyMetadataInfo 
* CompanyMetadataInfoArray 
* CreateVideoSitemapJob 
* PublishContext 
* PublishContextArray 
* SearchFilter 
* LongArray

**New Operations**

* applyMetadataTemplate 
* batchGetAssetPublishContexts 
* createCompanyMetadata 
* deleteCompanyMetadata 
* getCompanyMetadata 
* getPublishContexts 
* listCompanyMetadata 
* removeMask 
* removePropertySetPermissions 
* searchAssetsBySimilarity 
* searchAssetsByFulltext 
* setAssetPublishState 
* setPropertySetPermissions 
* updateAssetSet 
* updateCompanyMetadata 
* updateImageSet 
* updatePropertySetPermissions

**Modified Types**

* Changed `ActiveJob` to include a `createVideoSitemapJob` type 

* Changed `ScheduledJob` to include a `createVideoSitemapJob` type 

* Changed `ImageServingPublishJob` to include an optional `contextHandle`

* Changed `ImageRenderingPublishJob` to include an optional `contextHandle`

* Changed `MetadataField` to include an optional `initialTagField`

* Changed `MetadataCondition` to include and optional `caseSensitive` parameter 

* Changed `PropertySet` to include an optional `PermissionArray` as `permissions`

* Changed `UploadDirectoryJob` to include optional `xmpKeywords`, `xmpTemplateId` and `xmpTemplateOverride` parameters 

* Changed `VideoPublishJob` to include an optional `contextHandle`

**Modified Operations**

* Changed `createAssetSet` to include an optional `thumbAssetHandle`

* Changed `createImageSet` to include an optional `thumbAssetHandle`

* Changed `createMetadataField` to include an optional `initialTagValue` parameter 

* Changed `createPropertySet` to include an optional `PermissionUpdateArray` as `permissionArray`

* Changed `getImageServingPublishSettings` to include an optional `contextHandle` parameter 

* Changed `getImageRenderingPublishSettings` to include an optional `contextHandle` parameter 

* Changed `searchAssetsByFullText` to include a series of optional parameters:

    * `SearchFilter` as `filters` parameter 
    
    * `sortBy`
    * `sortDirection`

* Changed `searchAssetsByMetadata` to include a series of optional parameters:

    * `SearchFilter` as `filters` parameter 
    
    * `sortBy`
    * `sortDirection`
    * `haystackSearch` sequence of seven parameters

* Changed `setAssetPublishState` to include an optional `HandleArray` as `contextHandleArray`

* Changed `setImageServingPublishSettings` to include an optional `contextHandle` parameter 

* Changed `setImageRenderingPublishSettings` to include an optional `contextHandle`parameter 

* Changed `submitJob` to include an optional `createVideoSitemap` job type
