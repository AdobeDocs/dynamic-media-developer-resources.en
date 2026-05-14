---
description: Cache clustering allows multiple load-balanced servers to exchange cache entries in the primary response cache and the secondary data cache (for nested/embedded requests), with the potential to significantly increase server responsiveness by eliminating the need to generate the same cache entry on multiple servers.
solution: Experience Manager
title: Cache clustering
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d1bea565-ac4e-4717-a53f-cbe706664598
TQID: 'https://experienceleague.adobe.com/J1QtNEy9i67oveb1oS2V6-fagqrrlC30oih8AS1g-N4'
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
