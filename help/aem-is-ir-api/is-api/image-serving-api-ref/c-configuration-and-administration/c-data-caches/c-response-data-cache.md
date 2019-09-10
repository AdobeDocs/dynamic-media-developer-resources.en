---
description: The Platform Server caches all reply image and certain text data to disk unless a request is marked as non-cacheable.
seo-description: The Platform Server caches all reply image and certain text data to disk unless a request is marked as non-cacheable.
seo-title: Response data cache
solution: Experience Manager
title: Response data cache
topic: Scene7 Image Serving - Image Rendering API
uuid: dbfda210-3b50-4e8c-8d77-7263ae4e80a2
index: y
internal: n
snippet: y
---

# Response data cache{#response-data-cache}

The Platform Server caches all reply image and certain text data to disk unless a request is marked as non-cacheable.

The location of the Platform Server's disk cache is set with `PS::cache.rootPaths`.

For applications that have high cache hit rates, you can increase the server performance and capacity by distributing the response data cache among multiple disk devices. You accomplish this by creating a cache root folder on each disk and register them in `PS::cache.rootPaths`.

`PS::cache.maxSize` specifies the total size of all cache entries, not considering any file system overhead. The amount of disk space actually required depends on the file system properties-such as the disk block size-and the number of cache entries. It is recommended to reserve twice as much disk space for the HTTP disk cache as the amount specified by `PS::cache.maxSize`. A least-recently-used algorithm is employed to keep the amount of cached data within the limit.

In addition to `PS::cache.maxSize`, the response cache is also managed by limiting the maximum number of cache entries with `PS::cache.maxEntries`. On Linux, this setting must specify a value no larger than the number of available inodes on the cache partition.

>[!NOTE] {class="- topic/note "}
>
>The Platform Server maintains an in-memory cache index. The size of this index is 32 bytes times the value of `PS::cache.maxEntries`. You may need to increase the Platform Server heap size to accommodate larger caches.

The system uses a cache index file that is saved to disk when the server is shut down in an orderly fashion. In case of unexpected events such as a power failure, this file may not be saved. Also, it may take several minutes for the Platform Server to become ready. 
