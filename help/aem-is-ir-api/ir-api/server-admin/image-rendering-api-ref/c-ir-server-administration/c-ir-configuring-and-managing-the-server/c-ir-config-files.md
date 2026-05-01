---
description: Image Rendering configuration settings are stored in the [!DNL Platform Server] configuration file.
solution: Experience Manager
title: Configuration files
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 44ffebae-4933-455b-a902-4f6e7bb69184
TQID: https://experienceleague.adobe.com/sRbZm6LIQGVYFfmaq3A15ACjDO1qABkl6-6yhxfbYqE
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
# Configuration files{#configuration-files}

Image Rendering configuration settings are stored in the [!DNL Platform Server] configuration file.

The platform server configuration file is located at [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]. This file is a JAVA properties file. Care must be taken to follow the appropriate conventions, otherwise the [!DNL Platform Server] might fail to start. A double backslash (`\\`) or a single forward slash (/) must be used instead of a simple backslash (\) in Windows file paths, because the backslash is used as an escape character in this type of file. The file contains undocumented properties, which are for internal server use and must not be modified.

Refer to the [Configuration Settings Reference](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) for a list of all Image Rendering configuration settings.
