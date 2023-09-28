---
title: Response data cache
description: The [!DNL Platform Server] caches all reply images and certain text data to disk unless a request is marked as noncacheable.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: f09e596d-2b85-4950-8515-d54a2c2e86ae
---
# Response data cache{#response-data-cache}

The [!DNL Platform Server] caches all reply images and certain text data to disk unless a request is marked as non-cacheable.

The location of the [!DNL Platform Server]'s disk cache is set with `PS::cache.rootPaths`.

For applications that have high cache hit rates, you can increase the server performance and capacity by distributing the response data cache among multiple disk devices. You accomplish this by creating a cache root folder on each disk and register them in `PS::cache.rootPaths`.

The `PS::cache.maxSize` specifies the total size of all cache entries, not considering any file system overhead. The amount of disk space required depends on the file system properties-such as the disk block size-and the number of cache entries. Reserve twice as much disk space for the HTTP disk cache as the amount specified by `PS::cache.maxSize`. A least-recently-used algorithm is employed to keep the amount of cached data within the limit.

In addition to `PS::cache.maxSize`, the response cache is also managed by limiting the maximum number of cache entries with `PS::cache.maxEntries`. On Linux&reg;, this setting must specify a value no larger than the number of available inodes on the cache partition.

>[!NOTE]
>
>The [!DNL Platform Server] maintains an in-memory cache index. The size of this index is 32-bytes times the value of `PS::cache.maxEntries`. Increase the [!DNL Platform Server] heap size to accommodate larger caches, if necessary.

The system uses a cache index file that is saved to disk when the server is shut down in an orderly fashion. If there are unexpected events such as a power failure, this file may not be saved. Also, it may take several minutes for the [!DNL Platform Server] to become ready.
