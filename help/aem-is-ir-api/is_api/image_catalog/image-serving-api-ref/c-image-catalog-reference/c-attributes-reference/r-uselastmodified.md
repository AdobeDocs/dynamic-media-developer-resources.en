---
description: Enable last-modified response headers. Enables or disables inclusion of the Last-Modified header in cacheable HTTP responses emitted by Image Serving.
seo-description: Enable last-modified response headers. Enables or disables inclusion of the Last-Modified header in cacheable HTTP responses emitted by Image Serving.
seo-title: UseLastModified
solution: Experience Manager
title: UseLastModified
topic: Scene7 Image Serving - Image Rendering API
uuid: 43690bd8-2898-4c36-a126-8cc6c844e006
index: y
internal: n
snippet: y
---

# UseLastModified{#uselastmodified}

Enable last-modified response headers. Enables or disables inclusion of the Last-Modified header in cacheable HTTP responses emitted by Image Serving.

The server uses the most recent `catalog::TimeStamp` value of all catalogs/catalog records involved in a response as the Last-Modified header value.

Should be enabled only if a distributed caching network or other caching system is used which does not support etag headers.

>[!NOTE]
>
>Care must be taken when using Last-Modified headers in a load-balanced environment involving multiple Image Serving hosts. Client caching may be defeated and server load increase if for some reason the servers have different time stamps for the same catalog entries. Such a situation can occur as follows: 
>
>* Neither `catalog::TimeStamp` nor `attribute::TimeStamp`, so that the modification time of the [!DNL catalog.ini] file is used as the default for `catalog::TimeStamp`. 
>
>* Instead of sharing the image catalog files via a network mount, each server has its own instance of the catalog files on a local file system. 
>* Two or more instances of the same [!DNL catalog.ini] file have different file modification dates, possibly caused by improper copying of the files. 
>

## Properties {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

Flag. 0 to disable, 1 to enable Last-Modified HTTP headers.

## Default {#section-4eb47aadab8b41609bef296a4115f9f4}

Inherited from `default::UseLastModified` if not defined or if empty.

## See also {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catalog::TimeStamp](../../../../../is_api/image_catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) 
