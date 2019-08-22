---
description: All log files are written to the same log folder specified with TC directory.
seo-description: All log files are written to the same log folder specified with TC directory.
seo-title: Server logging
solution: Experience Manager
title: Server logging
topic: Scene7 Image Serving - Image Rendering API
uuid: 72075fd2-d50c-4094-b02b-3458efcd96dc
index: y
internal: n
snippet: y
---

# Server logging{#server-logging}

All log files are written to the same log folder specified with TC::directory.

Log files are typically created and rotated on a daily basis. Older log files in the log folder are automatically deleted after a specified number of days ( `TC::maxDays`).

Important A sufficient amount of disk space must be reserved for log files to avoid running out of disk space. 1-2 GB/day may be required for a heavily used server and default log settings.

The Platform Server and the Image Server create the three types of log files described below.

Other Image Serving components and certain other Scene7 packages, such as the Scene7 Viewers, may also create log files in the same folder. These log files are for Scene7 internal use and may be requested by Scene7 Support for trouble-shooting purposes.

## See also {#section-5ff5e46031b1461c92de24e632610d6d}

[Access Logging](../../../../is_api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f), [Debug/Trace Logging](../../../../is_api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82) 
