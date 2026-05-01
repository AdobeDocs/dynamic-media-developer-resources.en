---
description: While adding new data files is simple and straight-forward, special care must be taken when replacing existing data files which are actively used by the server. Instead of simply replacing such files, it is recommended to give the replacement file a new name (for example, append a version suffix to the file name). After the new file has been taken live, the old version can be deleted.
solution: Experience Manager
title: Deleting or replacing data files
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 1624e1b5-ba79-45db-8309-457a44fddab8
TQID: https://experienceleague.adobe.com/KSJn-SHE1w5NgxUlrJDIF3rpq-A3qhIG5G4gZ9qLhCw
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Deleting or replacing data files{#deleting-or-replacing-data-files}

While adding new data files is simple and straight-forward, special care must be taken when replacing existing data files which are actively used by the server. Instead of simply replacing such files, it is recommended to give the replacement file a new name (for example, append a version suffix to the file name). After the new file has been taken live, the old version can be deleted.

>[!NOTE]
>
>Data files should never be replaced or deleted while in active use by Image Serving. Errors or even a server crash may occur otherwise.

In all cases, remember that the [!DNL Platform Server] cache and the client cache entries must become stale before the updated data is seen by the client. Specific cache entries can be updated immediately using the `cache=validate` command.

Changes to font files and ICC profile files are not tracked directly by the cache manager. If such a resource is modified without changing its id, the server cache does not know about the change, and `cache=validate` does not cause the cache entry to be updated. `cache=update` can be used to force regenerating such cache entries.

To avoid the complications of replacing files, it is recommended to give a replacement file a new name and update the corresponding catalog entries. This allows replacing any data file while the server is live and cause server cache entries to become stale immediately with no additional intervention. This approach can be used for ICC profiles, fonts, and all images managed by image catalogs.
