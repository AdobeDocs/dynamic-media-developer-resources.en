---
description: Cache entries are refreshed automatically using either catalog-based or expiration-based cache validation, as selected with attribute CacheValidationPolicy (in default.ini or the .ini file of a specific image catalog).
solution: Experience Manager
title: Response cache validation
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
---

# Response cache validation{#response-cache-validation}

Cache entries are refreshed automatically using either catalog-based or expiration-based cache validation, as selected with attribute::CacheValidationPolicy (in default.ini or the .ini file of a specific image catalog).

 With catalog-based validation, an existing cache entry is considered stale if `catalog::LastModified` (or `attribute::LastModified`, or the file modification time of the [!DNL catalog.ini] file) is more recent than the time the cache entry was created.

With expiration-based validation, a cache entry becomes stale after 5 minutes since the most recent validation. In both cases, the server validates stale cache entries by checking the file dates of all image files that were involved with creating the request. If the file dates have not changed, the time stamp of the cache entry is updated and the cached date considered valid.

For typical applications that involve mostly images registered in image catalogs, catalog-based validation provides a performance advantage. Applications which do not involve image catalogs should use expiration-based cache validation. One way to achieve this is to set `attribute::cacheValidationPolicy=0` in [!DNL default.ini], and to `1` in all specific image catalog files.

Cache entries become invalid and are subject to re-generation when a catalog entry involved in the request changes in a way that would likely cause a change of the reply image. For example, the contents of `catalog::Modifier` changes.

>[!NOTE]
>
>Dynamic Media pyramid TIFF (PTIFF) images maintain the file date internally in the file header for validation purposes. The file modification time maintained by the file system is used to check if a non-PTIFF file has changed.

Only image files participate in the cache validation process. Changes to font files or ICC profile files do not cause automatic invalidation of cache entries. 
