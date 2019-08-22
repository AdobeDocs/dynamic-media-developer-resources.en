---
description: Static content source data files are accessed only by the Platform Server.
seo-description: Static content source data files are accessed only by the Platform Server.
seo-title: Static content source data
solution: Experience Manager
title: Static content source data
topic: Scene7 Image Serving - Image Rendering API
uuid: e3d21b3f-748e-4762-919f-9655940e3b30
index: y
internal: n
snippet: y
---

# Static content source data{#static-content-source-data}

Static content source data files are accessed only by the Platform Server.

 The path for static content data files is resolved as follows:

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

The server combines path segments right to left until an absolute file path is established.

All ` *[!DNL rootPath]*` segments can be empty, relative, or absolute path segments.

` *[!DNL catalogPath]*` is either an absolute or relative file path/name. *[!DNL requestPath]* must be a relative file path/name.

Multiple `PS::staticContent.rootPaths` values can be defined in [!DNL PlatformServer.conf]. This allows source data files to be distributed across multiple file systems. The Platform Server will try alternate paths in the order specified until the data file is found. 
