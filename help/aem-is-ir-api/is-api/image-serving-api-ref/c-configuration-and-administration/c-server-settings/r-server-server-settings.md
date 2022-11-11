---
description: Use these server settings to configure your server.
solution: Experience Manager
title: Server
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 10970ca8-b209-4adf-b027-6eb8d7a15db6
---
# Server{#server}

Use these server settings to configure your server.

## SV::ImageServerMode - Image Server Mode {#section-991b287f2dde4f77a24fc69d5b32cabd}

Both a 32- and a 64-bit version of the Image Server are available for Linux. Specify ImageServer64 when installed on 64-bit Linux servers, or ImageServer32 (default) when installed on 32-bit servers.

>[!NOTE]
>
>The 64-bit version of the Image Server does not support FlashPix source files.

>[!NOTE]
>
>64-bit mode is not supported on Windows. Only `ImageServer32` may be specified. Otherwise Image Serving will not start.

## SV::PsHeapSize - [!DNL Platform Server] Heap Size {#section-fd83715948764aeda58d6b3a9f9f8be9}

The Java heap size for the [!DNL Platform Server]. Defaults to " `512m`" (512 Mbytes).

## IS::TcpPort, PS::isConnection.port - Image Server Listening Port {#section-5421bfd2ca2a4a979faf812b6fdb2887}

Specifies the port used for communication between the [!DNL Platform Server] and the Image Server. Make sure to specify a port number which is not used otherwise on the host system.

>[!NOTE]
>
>For Image Serving to function correctly, the same value must be set for `IS::TcpPort` and `PS::isConnection.port`.

## IS::PhysicalMemory - Image Server Memory Limit {#section-85e37aa2ac6e456eb698da716dd3247d}

The approximate limit for in-memory image data, expressed as a percentage of physical memory. Valid range is 10% to 90%. The Image Server attempts to restrict its use of image memory to the specified amount if possible. The limit may be exceeded temporarily during heavy processing activity.

## IS::WorkerThreads - Number of Image Server Worker Threads {#section-e2946063b13c4f728cdf5dba3d8b4de1}

The maximum number of threads the Image Server uses for processing image data. Default is 0, which allows the Image Server to optimize the thread count automatically.

Some operating systems have threading models with a high context-switching overhead. In such a circumstance the overall server performance may improve when a specific thread count is selected (e.g. one thread per CPU). Some experimentation may be required to find the optimal setting. Refer to the Image Serving release notes and to the operating system documentation for additional information.

## IS::NumberOfTextServers - Number of Text Server Instances {#section-971e20a90c1a473598fba738ed95671a}

The maximum number of text renderers to be active concurrently. 0 (default) is equivalent to 1.5 times the number of available CPU cores.

## IS::TextServerTcpPortRange - Text Server Communication Ports {#section-a13465de88ed4df09931e5ba840c1942}

The ports to be used for text server communications. Specify the first and last port number, separated with '-'.
