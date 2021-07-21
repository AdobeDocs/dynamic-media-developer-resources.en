---
description: Use these server settings for the Image catalog service.
solution: Experience Manager
title: Image catalog service
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c089ef35-47a1-4921-8a5e-1ca78f29794d
---
# Image catalog service{#image-catalog-service}

Use these server settings for the Image catalog service.

## CS::catalog.rootPath - Image Catalog Folder {#section-02d107f157384b18835f884f24fea3aa}

Location of the image catalog folder (where all [!DNL catalog.ini] files must be located). Can be an absolute file path or a path relative to the *[!DNL install_folder]*. The server continuously monitors this folder and loads or reloads catalogs when a new main catalog file (with [!DNL .ini] file suffix) is detected or when the last modified time of an existing main catalog file has changed.

## CS::catalog.cacheRoot - Catalog Cache Folder {#section-73e499c3a5974f1aa4251e70272ff503}

The root folder for the catalog system cache. May be set to the same as one of the folders in `PS::cache.rootPaths`. The folder must be created manually before this setting is changed.

## CS::catalog.modificationWaitTime - Catalog File Parsing Delay {#section-7348065bcc124cb68ea947bf1b9b0845}

Time in msec the catalog service waits after a [!DNL catalog.ini] file is changed until it loads the secondary catalog files. This delay helps ensure that all secondary catalog files are up to date before the catalog service attempts to load them. Integer value in msec.

## CS::catalog.refreshInterval - Catalog File Check Frequency {#section-517fefc1d8784777a1026abec8630d58}

Frequency at which the catalog service will check for changes to image catalogs. Integer value in msec.
