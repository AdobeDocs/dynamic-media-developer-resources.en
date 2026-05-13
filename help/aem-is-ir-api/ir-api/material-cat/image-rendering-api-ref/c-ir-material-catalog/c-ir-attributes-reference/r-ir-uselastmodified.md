---
title: UseLastModified
description: Enable last-modified response headers. Enables or disables inclusion of the Last-Modified header in cacheable HTTP responses emitted by Image Rendering.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 31dfbc55-0efd-417b-be4a-67c878772388
TQID: 'https://experienceleague.adobe.com/X-d-02WckbxVyDxRvZDIcOghkk8Z8yYbGOZ3Aigx4ts'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# UseLastModified{#uselastmodified}

Enable last-modified response headers. Enables or disables inclusion of the Last-Modified header in cacheable HTTP responses emitted by Image Rendering.

The server uses the most recent `vignette::TimeStamp` and `catalog::TimeStamp` value of all vignette and material catalogs/catalog records involved in a response as the Last-Modified header value.

Should be enabled only if a distributed caching network, such as Akamai, is used which does not support etag headers.

>[!NOTE]
>
>Care must be taken when using Last-Modified headers in a load-balanced environment involving multiple Image Serving/Rendering hosts. Client caching may be defeated and server load increase if for some reason the servers have different time stamps for the same catalog entries. Such a situation can occur as follows:

* `catalog::TimeStamp`, `vignette::TimeStamp`, or `attribute::TimeStamp` is not defined, so that the modification time of the [!DNL catalog.ini] file is used as the default for `catalog::TimeStamp`. 

* Instead of sharing the material catalog files by way of a network mount, each server has its own instance of the catalog files on a local file system. 
* Two or more instances of the same [!DNL catalog.ini] file have different file modification dates, possibly caused by improper copying of the files.

## Properties {#section-453952244193452caccfaf7f601007c1}

Flag. 0 to disable, 1 to enable Last-Modified HTTP headers.

## Default {#section-ec8fae847ca2421d8cdcde324e5a2d76}

Inherited from `default::UseLastModified` if not defined or if empty.

## See also {#section-1536715169da48b0aecc4ab7326c86db}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
