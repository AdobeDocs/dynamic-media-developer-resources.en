---
description: Use these server settings for content data folders.
solution: Experience Manager
title: Content data folders
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9aa4121f-25f8-49d0-a304-7ae756c046f5
---
# Content data folders{#content-data-folders}

Use these server settings for content data folders.

## IS::RootPath - Image Data Root Folders {#section-5c57569514bb4d00b19de31d2e137e3b}

The location of all source data, including images, fonts, and ICC profiles. This can be one or more absolute file paths or paths relative to *[!DNL install_folder]*, separated with semicolons. If empty, *[!DNL install_folder]* is the default root. Multiple values can be specified to distribute image data across multiple file systems. The Image Server tries the root paths in the order specified until the requested file is found.

## PS::staticContent.rootPath - Static Content Data Root Folders {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

The location of static content source data which is intended to be delivered by way of the [!DNL /is/static] context. Can be one or more absolute file paths or paths relative to *[!DNL install_folder]*, separated with semicolons. If empty, *[!DNL install_folder]* is the default root.

Multiple values can be specified-separated by semi-colons-to distribute static contents across multiple file systems. Typically set to the same values as `IS::RootPath`.

The [!DNL Platform Server] tries the root paths in the order specified until the requested file is found.

>[!NOTE]
>
>By default, this field is intentionally set to a non-existing location ( [!DNL *[!DNL install_folder]*/static]), effectively disabling the static content service.

## IS::SaveDirectory - File Save Root Folder {#section-1c517f8d49ce4cb8b9013e520bf309c9}

The root path for `attribute::SavePath` (used by `req=saveToFile`). The Image Server must have create access permissions for the subfolder in which it creates image files.
