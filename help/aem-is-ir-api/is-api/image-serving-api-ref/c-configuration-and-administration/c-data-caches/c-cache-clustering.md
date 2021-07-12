---
description: Cache clustering allows multiple load-balanced servers to exchange cache entries in the primary response cache and the secondary data cache (for nested/embedded requests), with the potential to significantly increase server responsiveness by eliminating the need to generate the same cache entry on multiple servers.
solution: Experience Manager
title: Cache clustering
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: d1bea565-ac4e-4717-a53f-cbe706664598
---
# Cache clustering{#cache-clustering}

Cache clustering allows multiple load-balanced servers to exchange cache entries in the primary response cache and the secondary data cache (for nested/embedded requests), with the potential to significantly increase server responsiveness by eliminating the need to generate the same cache entry on multiple servers.

If so configured, when a server receives a request for an item which is not in local cache, it contacts the peer servers in the cluster. It checks to see if they already have that data item before asking the Image Server to generate the item.

Cache clustering primarily benefits applications involving highly cacheable contents. Server loads should be significantly reduced during initial deployment and when going live with new contents.

Timeouts and other safeguards ensure that the system continues to perform at full capacity even when one or more of the peer servers is offline.

The cache cluster can operate in one of two basic configurations:

* When `PS::cacheCluster.updateLocalCache` is enabled (default), any cache entry found on a peer server is copied to the local cache.

  This configuration reduces traffic between the peer servers. It also provides the fastest response times at the cost of having all cache entries replicated to all servers in the cluster. This is the recommended configuration. 

* When `PS::cacheCluster.updateLocalCache` is disabled, data from other servers in not copied to the local cache.

  This multiplies the available disk space for cache data. However, it increases the traffic between the peer servers and reduces the overall response times. Use this configuration only when you see low cache hit rates.
