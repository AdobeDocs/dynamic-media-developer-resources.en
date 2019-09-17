---
description: Use these server settings for cache clustering.
seo-description: Use these server settings for cache clustering.
seo-title: Cache clustering
solution: Experience Manager
title: Cache clustering
topic: Scene7 Image Serving - Image Rendering API
uuid: ed6335d7-26c9-45d8-95f6-6c05e788e449
---

# Cache clustering{#cache-clustering}

Use these server settings for cache clustering.

## PS::cacheCluster.hosts - Hosts {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

List of IP addresses, separated by semi-colons. Include the IP addresses of all peer servers from which this host should obtain cache data. The IP address of the local host may be included for convenience; this allows the same configuration settings for all servers in the cluster.

## PS::cacheCluster.updateLocalCache - Update Local Cache {#section-154c2c0af4544200a3499232bb130dde}

Set to 'Yes' if a cache entry provided by a peer server should be copied to the local response cache.

## PS::cacheCluster.queryTimeout - Query Timeout {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

When requesting a cache entry from peer servers, the server will wait until one server responds that it has this particular data item, or until all peer servers have responded that they do not have the data item, or until the time specified with this setting (in msec) has expired.

## PS::cacheCluster.fetchTimeout - Fetch Timeout {#section-41c42a29a26f43dc9cff50ad9fae1f14}

Specifies the maximum number of msec the server will wait for the actual cache data to be delivered from the peer server. If the full data has not been delivered before the timeout expires, the server assumes that the peer has become unavailable. The cache entry is then generated locally. 
