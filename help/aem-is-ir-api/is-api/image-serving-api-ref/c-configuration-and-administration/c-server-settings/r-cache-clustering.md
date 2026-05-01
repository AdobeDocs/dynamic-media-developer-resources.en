---
description: Use these server settings for cache clustering.
solution: Experience Manager
title: Cache clustering
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: bd0267e7-ebf5-4995-b55e-89cb1a58de6d
TQID: https://experienceleague.adobe.com/nc7lN72GE1-147fnWlfhz3TiFYHCs7uebdm-8Ie0xX8
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

Use these server settings for cache clustering.

## PS::cacheCluster.hosts - Hosts {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

List of IP addresses, separated by semi-colons. Include the IP addresses of all peer servers from which this host should obtain cache data. The IP address of the local host may be included for convenience; this allows the same configuration settings for all servers in the cluster.

## PS::cacheCluster.updateLocalCache - Update Local Cache {#section-154c2c0af4544200a3499232bb130dde}

Set to 'Yes' if a cache entry provided by a peer server should be copied to the local response cache.

## PS::cacheCluster.queryTimeout - Query Timeout {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

When requesting a cache entry from peer servers, the server waits until one server responds that it has this particular data item, or until all peer servers have responded that they do not have the data item, or until the time specified with this setting (in msec) has expired.

## PS::cacheCluster.fetchTimeout - Fetch Timeout {#section-41c42a29a26f43dc9cff50ad9fae1f14}

Specifies the maximum number of msec the server waits for the actual cache data to be delivered from the peer server. If the full data has not been delivered before the timeout expires, the server assumes that the peer has become unavailable. The cache entry is then generated locally.
