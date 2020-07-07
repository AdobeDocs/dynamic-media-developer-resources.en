---
description: Enable last-modified response headers. Enables or disables inclusion of the Last-Modified header in cacheable HTTP responses emitted by Image Rendering.
seo-description: Enable last-modified response headers. Enables or disables inclusion of the Last-Modified header in cacheable HTTP responses emitted by Image Rendering.
seo-title: UseLastModified
solution: Experience Manager
title: UseLastModified
topic: Scene7 Image Serving - Image Rendering API
uuid: f2ce2e04-4133-40af-ac82-cae57b253fe9
---

# UseLastModified{#uselastmodified}

Enable last-modified response headers. Enables or disables inclusion of the Last-Modified header in cacheable HTTP responses emitted by Image Rendering.

The server uses the most recent `vignette::TimeStamp` and `catalog::TimeStamp` value of all vignette and material catalogs/catalog records involved in a response as the Last-Modified header value.

Should be enabled only if a distributed caching network, such as Akamai, is used which does not support etag headers.

>[!NOTE]
>
>Care must be taken when using Last-Modified headers in a load-balanced environment involving multiple Image Serving/Rendering hosts. Client caching may be defeated and server load increase if for some reason the servers have different time stamps for the same catalog entries. Such a situation can occur as follows:

* Neither `catalog::TimeStamp`, `vignette::TimeStamp`, nor `attribute::TimeStamp` is defined, so that the modification time of the [!DNL catalog.ini] file is used as the default for `catalog::TimeStamp`. 

* Instead of sharing the material catalog files via a network mount, each server has its own instance of the catalog files on a local file system. 
* Two or more instances of the same [!DNL catalog.ini] file have different file modification dates, possibly caused by improper copying of the files.

## Properties {#section-453952244193452caccfaf7f601007c1}

Flag. 0 to disable, 1 to enable Last-Modified HTTP headers.

## Default {#section-ec8fae847ca2421d8cdcde324e5a2d76}

Inherited from `default::UseLastModified` if not defined or if empty.

## See also {#section-1536715169da48b0aecc4ab7326c86db}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1) 
