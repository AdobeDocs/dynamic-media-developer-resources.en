---
description: Vignette files can be replaced or deleted while the server is live by using the req=release command just before the file is overwritten.
seo-description: Vignette files can be replaced or deleted while the server is live by using the req=release command just before the file is overwritten.
seo-title: Deleting or replacing source data files
solution: Experience Manager
title: Deleting or replacing source data files
uuid: 13dc0489-7ab0-481e-b213-214affe9819e
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Administrator,Business Practitioner"
---

# Deleting or replacing source data files{#deleting-or-replacing-source-data-files}

Vignette files can be replaced or deleted while the server is live by using the req=release command just before the file is overwritten.

>[!NOTE]
>
>A data file must not be replaced or deleted while the Render Server is accessing it.

Keep in mind that deleting or replacing a source data file only causes the Render Server to close the file until the next request that accesses that vignette. Several retries may be necessary if a file is heavily used.

The Render Server must be stopped to replace other data files.

Platform Server cache entries are automatically invalidated when material files or vignettes are replaced. Replacing ICC profile files does not invalidate caches.

To avoid the complications of replacing files, it is recommended to give a replacement file a new name and update the corresponding catalog entries. This allows replacing any data file while the server is live and causes server cache entries to become stale automatically with no additional intervention. This approach can be used for all data files managed by image catalogs. 
