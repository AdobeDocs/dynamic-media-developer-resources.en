---
description: The settings in this section need to be considered only if SVG rendering is required.
solution: Experience Manager
title: SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 2863cc86-1f79-4db3-bd6f-a42839ef3439
---
# SVG{#svg}

The settings in this section need to be considered only if SVG rendering is required.

## SV::SvgHeapSize - SVG Heap Size {#section-59ab17681daa4be8b5d794713e1a504e}

The Java heap size for the SVG Renderer. Defaults to "200m" (200 Mbytes).

## PS::svgProvider.rootPaths - SVG Data Root Folders {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

The location of the SVG source data files. Can be one or more absolute file paths or paths relative to *[!DNL install_folder]*, separated with semicolons. Typically set to the same value as `IS::RootPath`.

## PS::svgProvider.SVGFileSizeLimit - Maximum SVG File Size {#section-b9c81e3e104642ebbdd9f000843d3256}

Maximum SVG source file size in kBytes. The server returns an error when an attempt is made to render an SVG file which is larger than this limit. Default is 1024 kbytes.

## IS::SvgMAxRenderRgnPixels - SVG Output Image Size Limit {#section-5be1fd9639424d878a5ffd11736d3920}

Limits the size of images SVGRender can produce. Integer value larger than 0 in millions of pixels. An error is returned if a render operation would exceed the size limit. Default is 4.

## PS::svgProvider.port - Platform Server Listening Port {#section-f7e42a96c2dd4523b46f0557c239e659}

The port used for SvgRender to obtain images from the Platform Server to be embedded in SVG renderings.

Important For correct functioning of the SVGRender component, this configuration option must be set to the same value as `TC::PsPort`.

## PS::svgProvider.fontRoot - SVG Font Files Folder {#section-a8d45b0d68504945b8780f5eac351b0d}

Specifies where the SvgRender will find the font files needed for rendering SVG text; typically one of the paths specified in `IS::RootPaths`. Default is [!DNL  *[!DNL install_folder]*/images].

## SVG::SVGRender.port, IS::SVGTcpPort - SVG Communications Port {#section-608687123aa644b7b58fe42385d71b79}

Configures the port on which the Image Server and the SVGRender component communicate.

>[!NOTE]
>
>For correct functioning of the SVGRender component, the same port number must be specified for `SVG::SVGRender.port` and `IS::SVGTcpPort`.
