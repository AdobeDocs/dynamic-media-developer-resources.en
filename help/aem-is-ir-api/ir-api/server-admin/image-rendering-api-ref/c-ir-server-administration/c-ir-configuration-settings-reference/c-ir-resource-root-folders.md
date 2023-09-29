---
title: Resource root folders (ir.resourceRootPaths)
description: A list of paths, delimited by semi-colons, serve as roots for all data files with relative file paths.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
---
# Resource root folders (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

A list of paths, delimited by semi-colons, serve as roots for all data files with relative file paths.

It can either be absolute paths or paths relative to *[!DNL install_folder]*. When multiple paths are specified, the server tries each root in the given order until the file is found. The default is [!DNL ./resources], for a default root path of [!DNL install_folder/resources].
