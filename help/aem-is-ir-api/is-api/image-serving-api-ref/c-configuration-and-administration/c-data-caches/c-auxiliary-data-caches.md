---
description: Intermediate image data produced by nested/embedded Image Serving and Image Rendering requests can be cached by specifying cache=on in the nested/embedded request. This data is stored in proprietary format in the response data cache.
solution: Experience Manager
title: Auxiliary data caches
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 39906c86-fd9e-4961-a8ba-2ac44c4214a2
---
# Auxiliary data caches{#auxiliary-data-caches}

Intermediate image data produced by nested/embedded Image Serving and Image Rendering requests can be cached by specifying cache=on in the nested/embedded request. This data is stored in proprietary format in the response data cache.

Images obtained from foreign HTTP servers are also stored in the response data cache. Such images are validated automatically with the validate utility before the cache entry is generated.

The Platform Server compiles image catalog data for efficient access. This data is stored in `CS::CatalogCacheFolder`.
