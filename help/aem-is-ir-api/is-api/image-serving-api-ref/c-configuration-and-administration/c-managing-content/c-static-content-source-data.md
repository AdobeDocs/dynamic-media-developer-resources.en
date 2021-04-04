---
description: Static content source data files are accessed only by the Platform Server.
solution: Experience Manager
title: Static content source data
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
---
# Static content source data{#static-content-source-data}

Static content source data files are accessed only by the Platform Server.

 The path for static content data files is resolved as follows:

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

The server combines path segments right to left until an absolute file path is established.

All ` *[!DNL rootPath]*` segments can be empty, relative, or absolute path segments.

` *[!DNL catalogPath]*` is either an absolute or relative file path/name. *[!DNL requestPath]* must be a relative file path/name.

Multiple `PS::staticContent.rootPaths` values can be defined in [!DNL PlatformServer.conf]. This allows source data files to be distributed across multiple file systems. The Platform Server will try alternate paths in the order specified until the data file is found.
