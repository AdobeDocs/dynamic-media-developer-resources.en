---
description: This documentation explains how to administer the Dynamic Media Image Rendering server.
solution: Experience Manager
title: Server administration overview
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 294cd068-8676-4932-a3ad-1a3c5bfa691e
TQID: https://experienceleague.adobe.com/2ozd0Uj6lg-kjK-kUQd-hvZ5cVqMNSUaZ5LZU90qof0
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
# Server administration overview{#server-administration-overview}

This documentation explains how to administer the Dynamic Media Image Rendering server.

Image Rendering consists of two major components:

* A Java package is deployed with the Image Serving [!DNL Platform Server] and manages client connection, caching, material catalogs. 
* A native code module is deployed as an extension library for the Image Server and implements the core image rendering functionalities.

Both components are collectively called the *Render Server*.

Image Rendering shares many server facilities with Image Serving, and all options are configured by editing a configuration file. Additional configuration attributes are provided by the default catalog ( [!DNL default.ini]) or specific material catalogs. See Material Catalogs for details.

The Image Rendering install folder ( *[!DNL install_folder]*) is [!DNL *[!DNL install_root]*/ImageRendering]. On Windows, the default *[!DNL install_root]* is `C:\Program Files\Scene7`. A different folder may be specified during installation. On Linux, *[!DNL install_root]* must always be [!DNL /usr/local/scene7]. Symbolic links may be used.

All file paths are case-sensitive on UNIX and case-insensitive on Windows.
