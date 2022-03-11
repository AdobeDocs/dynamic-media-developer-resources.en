---
title: Deprecated calls
description: Image Production System API calls and their associated parameters that are no longer used or supported in Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
---
# Deprecated calls{#deprecated-calls}

Image Production System API calls and their associated parameters that are no longer used.

## Deprecated calls {#topic-654c0466e6434fe4a95953322255b08c}

Image Production System API calls and their associated parameters that are no longer used in Dynamic Media.

* `ExcludeMasterVideoFromAVS` - Deprecated from [Data types](/help/aem-ips-api/types/c-data-types/c-data-types.md). This parameter excluded the primary video from the adaptive video set. 
   >[!IMPORTANT]
   >
   >Adobe is ending support for this parameter on September 1, 2022. See also [ExcludeMasterVideoFromAVS](/help/aem-ips-api/types/c-data-types/r-exclude-master-video-from-avs.md).
* `addMediaPortalEvent` - Deprecated from [Operations](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). This parameter let you add a Media Portal Event to IPS.  
* `getMediaPortalEvent` - Deprecated from [Operations](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). This parameter let you get media portal events that matched specified criteria.  
* `getCdnCacheInvalidationStatus` - Deprecated from [Operations](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). This parameter is now deprecated because the `cdnCacheInvalidation` parameter invalidates the cache almost immediately (~5 seconds). As such, polling for invalidation status is no longer required.
