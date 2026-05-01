---
description: Image catalogs are used to provide information about images and supporting data (such as fonts and ICC profiles) to the server.
solution: Experience Manager
title: Overview
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36cdd833-6fcb-4be6-a4f8-ba8d20580f29
TQID: https://experienceleague.adobe.com/uThjVWkmajxVqyr7-PlqLWTrZjbvS8MAIiwY0zuanXM
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
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
---
# Overview{#overview}

Image catalogs are used to provide information about images and supporting data (such as fonts and ICC profiles) to the server.

 Image catalogs are used to provide information about images and supporting data (such as fonts and ICC profiles) to the server.

Each image catalog consists of a required catalog attribute file and a set of optional catalog data files:

* The image data file, which itemizes images and templates and their associated metadata. 
* The SVG data file, which itemizes SVG files and their associated metadata. 
* The macro definitions file, which provides definitions for request macros. 
* The font map file, which keeps track of text fonts. 
* The profile map file, which itemizes ICC color profiles. 
* The rule set file, which defines HTTP request pre-processing rules.

Catalog data files are associated with image catalogs by file references in the catalog attribute file. The same catalog data file can be shared by multiple image catalogs.

Catalog attribute files must have an [!DNL .ini] file suffix and must be located in the [!DNL Platform Server]'s catalog folder ( `PlatformServer::catalog.rootPath`). Catalog data files can be located in the same folder or any other folder accessible to the [!DNL Platform Server].

This document describes the Image Catalog file format for the Dynamic Media Image Serving system. The intended audience is experienced programmers and web site developers who want to leverage Dynamic Media Image Serving for a web or custom application.

It is assumed that the reader is generally familiar with the Dynamic Media Image Serving system, general HTTP protocol standards and conventions, and basic imaging terminology.
