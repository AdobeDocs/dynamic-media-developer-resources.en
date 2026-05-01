---
description: Use these server settings for server caches.
solution: Experience Manager
title: Server caches
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 6a8d44d3-ecac-4fe0-9f81-28b1cd55e7e1
TQID: https://experienceleague.adobe.com/UpO6aeF4ysSInXK6gKez6FCKqqmEmjhc-PtkPQTYHpU
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
# Server caches{#server-caches}

Use these server settings for server caches.

## PS::cache.rootPaths - Cache Data Folders {#section-f0aa808304d74ecdb0c3644f11906c53}

The root folder(s) for the [!DNL Platform Server]'s disk cache. One or more absolute file paths or paths relative to *[!DNL install_folder]*, separated by semicolons (;). The data for the HTTP response cache is distributed evenly across all specified folders. The caches for the auxiliary caches (compiled image catalogs and foreign image data) are located in the primary cache folder (the first folder in the list).

## PS::cache.maxSize - Response Data Cache Size {#section-ed2e1e7ba4bd4e13b77bb20c4cacddb4}

The maximum size of the HTTP response cache in bytes. This setting limits the amount of actual data to be cached; it does not consider file system overhead. (See [Response Data Cache](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-data-caches/c-response-data-cache.md#concept-81ea996c242441f2a69f7e9d9b3a29ca).) If multiple cache data folders are specified, the cache data is spread evenly across all folders. The value of `cache.maxSize` in [!DNL PlatformServer.conf] is in bytes.

## PS::cache.maxEntries - Response Data Cache Max Entries {#section-5603e327e90542a5b50aeeb27b080410}

The number of entries allocated for the in-memory HTTP response cache index.

>[!NOTE]
>
>On Linux, make sure that sufficient i-nodes are allocated for the cache partition to avoid running out of i-nodes.

## IS::TempDirectory - Image Server Temporary Files Folder {#section-42ea1e7a68c444878f7245c5bbcb1672}

The Image Server occasionally needs to save intermediate data to disk. The path can be absolute or relative to *[!DNL install_folder]*.

>[!NOTE]
>
>The new folder must be created before changing this setting. Make sure the access permissions are set so that the Image Server has full control of the folder.

## SV::temp - Server Supervisor Temporary Files Folder {#section-fd2cd5ef7e814a4bb56aaf5525e1a154}

The Server Supervisor occasionally needs to save intermediate data to disk. The path can be absolute or relative to *[!DNL install_folder]*. Defaults to [!DNL  *[!DNL install_folder]*/temp].

>[!NOTE]
>
>The new folder must be created before changing this setting. Make sure the access permissions are set so that the Server Supervisor has full control of the folder.
