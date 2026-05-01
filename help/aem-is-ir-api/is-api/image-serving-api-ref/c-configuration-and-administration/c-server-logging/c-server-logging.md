---
description: All log files are written to the same log folder specified with TC directory.
solution: Experience Manager
title: Server logging
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 5be30dd6-e540-4189-9379-7465ac7198ce
TQID: https://experienceleague.adobe.com/9CDhwgLXFqpIfa6m6SVZ6Y0FGTC5rO45pbwpIFo9eF8
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Server logging{#server-logging}

All log files are written to the same log folder specified with TC::directory.

Log files are typically created and rotated on a daily basis. Older log files in the log folder are automatically deleted after a specified number of days ( `TC::maxDays`).

Important A sufficient amount of disk space must be reserved for log files to avoid running out of disk space. 1-2 GB/day may be required for a heavily used server and default log settings.

The [!DNL Platform Server] and the Image Server create the three types of log files described below.

Other Image Serving components and certain other Dynamic Media packages, such as the Dynamic Media Viewers, may also create log files in the same folder. These log files are for Dynamic Media internal use and may be requested by Dynamic Media technical support for trouble-shooting purposes.

* [Access log](c-access-log.md)
* [Trace log](c-trace-log.md)
* [Image Server log](c-image-server-log.md)

## See also {#section-5ff5e46031b1461c92de24e632610d6d}

[Access Logging](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f), [Debug/Trace Logging](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
