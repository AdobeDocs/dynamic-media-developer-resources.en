---
description: The server continuously monitors the catalog folder and automatically reloads an image catalog, including the associated catalog data files, when it detects that the main catalog attribute file has been changed.
solution: Experience Manager
title: Updating image catalogs
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b520b4f3-6717-4768-99e2-78a76d1ede24
---
# Updating image catalogs{#updating-image-catalogs}

The server continuously monitors the catalog folder and automatically reloads an image catalog, including the associated catalog data files, when it detects that the main catalog attribute file has been changed.

 To update image catalogs on the server, first replace all catalog data files that need to be changed, and then replace (or "touch," to update the file date) the catalog attributes file to trigger the catalog reload.

## Incremental updates {#section-2c0f2c1b8480486d86920b5f2cfe72d2}

Loading and processing large image catalogs can place a substantial load on the server, and may have a negative impact on live serving operations. To minimize this impact, it is recommended to implement an incremental catalog update mechanism, which works as follows:

A primary catalog file containing all images is loaded nightly during low traffic hours. If it is necessary during the day to add or change records in the image catalog, another image data file is created which contains only the new or changed records. This file is registered as a secondary image data file in `attribute::CatalogFile`. The server detects that the catalog attribute file has changed, and then checks which catalog data files have changed. If the main image data file has not been touched, the server loads or reloads only the incremental data file. Because this file is typically much smaller than the main catalog file, the impact on the server is much reduced, compared with reloading the main catalog.

Incremental updates can significantly reduce impact on the server during heavy traffic. It is recommended to regularly merge the incremental catalog data file into the main catalog data file during low-traffic hours to maintain optimal server performance.
