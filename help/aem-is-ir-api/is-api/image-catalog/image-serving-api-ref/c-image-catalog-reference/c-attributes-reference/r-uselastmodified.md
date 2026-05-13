---
description: Enable last-modified response headers. Enables or disables inclusion of the Last-Modified header in cacheable HTTP responses emitted by Image Serving.
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4908da5d-636e-44d2-bd49-40e01c8b5f79
TQID: 'https://experienceleague.adobe.com/jmwz9jThBnFtTZBRoI0kbKwoxf1MU7rn1CpKrSU4f04'
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

Enable last-modified response headers. Enables or disables inclusion of the Last-Modified header in cacheable HTTP responses emitted by Image Serving.

The server uses the most recent `catalog::TimeStamp` value of all catalogs/catalog records involved in a response as the Last-Modified header value.

Should be enabled only if a distributed caching network or other caching system is used which does not support etag headers.

>[!NOTE]
>
>Care must be taken when using Last-Modified headers in a load-balanced environment involving multiple Image Serving hosts. Client caching may be defeated and server load increase if for some reason the servers have different time stamps for the same catalog entries. Such a situation can occur as follows: 
>
>* Neither `catalog::TimeStamp` nor `attribute::TimeStamp`, so that the modification time of the [!DNL catalog.ini] file is used as the default for `catalog::TimeStamp`. 
>
>* Instead of sharing the image catalog files by way of a network mount, each server has its own instance of the catalog files on a local file system. 
>* Two or more instances of the same [!DNL catalog.ini] file have different file modification dates, possibly caused by improper copying of the files. 
>

## Properties {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

Flag. 0 to disable, 1 to enable Last-Modified HTTP headers.

## Default {#section-4eb47aadab8b41609bef296a4115f9f4}

Inherited from `default::UseLastModified` if not defined or if empty.

## See also {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
