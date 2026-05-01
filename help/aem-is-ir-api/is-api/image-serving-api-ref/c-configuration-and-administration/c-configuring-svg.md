---
description: The SvgRender component is an independent Java application.
solution: Experience Manager
title: Configuring SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9013e13f-818f-41b4-80b6-2615d9a8742f
TQID: https://experienceleague.adobe.com/d1OjO-WHx6BhLQihMKMdI9xYhWIvdf21u4o-IEXrS0g
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
# Configuring SVG{#configuring-svg}

The SvgRender component is an independent Java application.

SVG configuration settings are located in [!DNL PlatformServer.conf], [!DNL SVG.conf], [!DNL ImageServerRegistry.xml], and [!DNL ServerSupervisorRegistry.xml].

A socket connection is used to communicate between SvgRender and the Image Server. The port number is 27346. If necessary, it can be changed by setting `SVGRender.port` in [!DNL svg.conf] and `<SVGTcpPort>` in [!DNL ImageServerRegistry.xml] to a new value.

## See also {#section-c085b47d54d44059bdaa67fd5e226e91}

[SVG Configuration Settings](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
