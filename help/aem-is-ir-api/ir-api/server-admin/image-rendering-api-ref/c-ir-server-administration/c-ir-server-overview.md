---
description: This documentation explains how to administer the Dynamic Media Image Rendering server.
solution: Experience Manager
title: Server administration overview
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
---

# Server administration overview{#server-administration-overview}

This documentation explains how to administer the Dynamic Media Image Rendering server.

Image Rendering consists of two major components:

* A Java package is deployed with the Image Serving Platform Server and manages client connection, caching, material catalogs. 
* A native code module is deployed as an extension library for the Image Server and implements the core image rendering functionalities.

Both components are collectively called the *Render Server*.

Image Rendering shares many server facilities with Image Serving, and all options are configured by editing a configuration file. Additional configuration attributes are provided by the default catalog ( [!DNL default.ini]) or specific material catalogs. See Material Catalogs for details.

The Image Rendering install folder ( *[!DNL install_folder]*) is [!DNL *[!DNL install_root]*/ImageRendering]. On Windows, the default *[!DNL install_root]* is `C:\Program Files\Scene7`. A different folder may be specified during installation. On Linux, *[!DNL install_root]* must always be [!DNL /usr/local/scene7]. Symbolic links may be used.

All file paths are case-sensitive on UNIX and case-insensitive on Windows. 
