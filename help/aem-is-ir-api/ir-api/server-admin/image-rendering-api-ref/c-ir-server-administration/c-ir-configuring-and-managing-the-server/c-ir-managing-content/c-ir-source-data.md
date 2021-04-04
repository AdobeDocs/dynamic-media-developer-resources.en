---
description: Image Rendering source data files include vignette files, material files (images for repeatable textures and decals as well as cabinet and window covering style files), and ICC profiles.
solution: Experience Manager
title: Source data
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: de2d8fa2-6793-49ba-b873-adf723369cce
---
# Source data{#source-data}

Image Rendering source data files include vignette files, material files (images for repeatable textures and decals as well as cabinet and window covering style files), and ICC profiles.

 All source data files must be accessible to the native code component of Image Rendering (co-located with the Image Server).

If a material catalog is involved, the file specified in the material catalog (with `vignette::Path`, `catalog::Path`, or `icc::ProfilePath`) is looked up by the Render Server as follows:

* If the path is absolute, it is used as is. 
* If the path is relative, it is prefixed with `catalog::RootPath` (from a named material catalog). 
* If the path is absolute, it is used; otherwise, it is prefixed with `default::RootPath` (from the default catalog). 
* If the path is absolute, it is used; otherwise, the server combines it with the path specified in [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2). 
* If the path is now absolute, it is used; otherwise, it is assumed to be relative to [!DNL  *[!DNL install_folder]*].

If no image catalog is involved, the path is combined with `default::RootPath` and then processed as above.

The physical location of source data files is typically specified with [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2). Multiple values can be specified to allow source data files to be distributed across multiple file systems. The Render Server will try each path in the order specified until the data file is found.

New data files of any kind can be added anytime without stopping the server.
