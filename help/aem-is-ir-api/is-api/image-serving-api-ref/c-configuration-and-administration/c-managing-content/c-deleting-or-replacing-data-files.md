---
description: While adding new data files is simple and straight-forward, special care must be taken when replacing existing data files which are actively used by the server. Instead of simply replacing such files, it is recommended to give the replacement file a new name (for example, append a version suffix to the file name). After the new file has been taken live, the old version can be deleted.
solution: Experience Manager
title: Deleting or replacing data files
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 1624e1b5-ba79-45db-8309-457a44fddab8
---
# Deleting or replacing data files{#deleting-or-replacing-data-files}

While adding new data files is simple and straight-forward, special care must be taken when replacing existing data files which are actively used by the server. Instead of simply replacing such files, it is recommended to give the replacement file a new name (for example, append a version suffix to the file name). After the new file has been taken live, the old version can be deleted.

>[!NOTE]
>
>Data files should never be replaced or deleted while in active use by Image Serving. Errors or even a server crash may occur otherwise.

In all cases, remember that the [!DNL Platform Server] cache and the client cache entries must become stale before the updated data is seen by the client. Specific cache entries can be updated immediately using the `cache=validate` command.

Changes to font files and ICC profile files are not tracked directly by the cache manager. If such a resource is modified without changing its id, the server cache does not know about the change, and `cache=validate` does not cause the cache entry to be updated. `cache=update` can be used to force regenerating such cache entries.

To avoid the complications of replacing files, it is recommended to give a replacement file a new name and update the corresponding catalog entries. This allows replacing any data file while the server is live and cause server cache entries to become stale immediately with no additional intervention. This approach can be used for ICC profiles, fonts, and all images managed by image catalogs.
