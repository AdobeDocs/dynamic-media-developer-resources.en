---
description: All log files are written to the same log folder specified with TC directory.
solution: Experience Manager
title: Server logging
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 5be30dd6-e540-4189-9379-7465ac7198ce
---
# Server logging{#server-logging}

All log files are written to the same log folder specified with TC::directory.

Log files are typically created and rotated on a daily basis. Older log files in the log folder are automatically deleted after a specified number of days ( `TC::maxDays`).

Important A sufficient amount of disk space must be reserved for log files to avoid running out of disk space. 1-2 GB/day may be required for a heavily used server and default log settings.

The Platform Server and the Image Server create the three types of log files described below.

Other Image Serving components and certain other Dynamic Media packages, such as the Dynamic Media Viewers, may also create log files in the same folder. These log files are for Dynamic Media internal use and may be requested by Dynamic Media technical support for trouble-shooting purposes.

* [Access log](c-access-log.md)
* [Trace log](c-trace-log.md)
* [Image Server log](c-image-server-log.md)

## See also {#section-5ff5e46031b1461c92de24e632610d6d}

[Access Logging](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f), [Debug/Trace Logging](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
