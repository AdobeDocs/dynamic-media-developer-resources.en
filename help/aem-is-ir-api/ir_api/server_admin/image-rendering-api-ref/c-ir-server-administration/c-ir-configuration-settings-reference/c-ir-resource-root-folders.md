---
description: List of paths, delimited by semi-colons, serve as roots for all data files with relative file paths.
seo-description: List of paths, delimited by semi-colons, serve as roots for all data files with relative file paths.
seo-title: Resource root folders (ir.resourceRootPaths)
solution: Experience Manager
title: Resource root folders (ir.resourceRootPaths)
topic: Scene7 Image Serving - Image Rendering API
uuid: 78284325-d288-49a6-86e6-2d278d14dd1e
index: y
internal: n
snippet: y
---

# Resource root folders (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

List of paths, delimited by semi-colons, serve as roots for all data files with relative file paths.

Can either be absolute paths or paths relative to [!DNL *[!DNL install_folder]*]. When multiple paths are specified, the server will try each root in the given order until the file is found. Default is [!DNL ./ resources], for a default root path of [!DNL *[!DNL install_folder]*/resources]. 
