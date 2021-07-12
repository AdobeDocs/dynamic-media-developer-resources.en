---
description: The SvgRender component is an independent Java application.
solution: Experience Manager
title: Configuring SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 9013e13f-818f-41b4-80b6-2615d9a8742f
---
# Configuring SVG{#configuring-svg}

The SvgRender component is an independent Java application.

SVG configuration settings are located in [!DNL PlatformServer.conf], [!DNL SVG.conf], [!DNL ImageServerRegistry.xml], and [!DNL ServerSupervisorRegistry.xml].

A socket connection is used to communicate between SvgRender and the Image Server. The port number is 27346. If necessary, it can be changed by setting `SVGRender.port` in [!DNL svg.conf] and `<SVGTcpPort>` in [!DNL ImageServerRegistry.xml] to a new value.

## See also {#section-c085b47d54d44059bdaa67fd5e226e91}

[SVG Configuration Settings](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
