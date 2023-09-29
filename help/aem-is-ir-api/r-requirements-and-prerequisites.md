---
title: System requirements and prerequisites
description: Before using Dynamic Media Image Serving, make sure that your system meets the system requirements.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2dfec9-0a42-4ccb-8442-6f7c4a39eda1
---
# System requirements and prerequisites{#system-requirements-and-prerequisites}

Before using Dynamic Media Image Serving, make sure that your system meets the system requirements.

## Server hardware {#section-f3c14a7bc1b745118602659628df779f}

Your server should meet the following hardware requirements.

>[!NOTE]
>
>Systems with processors featuring AMD64 and Intel&reg; EM64T are typically configured as NUMA (Non-Uniform Memory Architecture) platforms. This means that the kernel constructs multiple memory nodes at boot-time rather than constructing a single memory node. The multiple node construct can result in memory exhaustion on one or more of the nodes before other nodes become exhausted. When memory exhaustion happens the kernel can decide to kill processes (for example, the Image Server or [!DNL Platform Server]) even though there is available memory. Therefore, Adobe recommends that if you are running such a system you turn off NUMA. Use the `numa=off` start option to avoid the kernel stopping these processes.

**Windows**

* Intel Xeon&reg; or AMD&reg; Opteron CPU with at least four cores. 
* 1 GB of RAM minimum. 
* Swap space is equal to at least twice the amount of physical memory (RAM). 
* 2 GB of available hard disk space for installation and basic operation, additional disk space is required for source images, logs, data caches, and manifest files. 
* Fast Ethernet Network Interface Card.

**Linux&reg;**

* Intel Xeon&reg; or AMD&reg; Opteron CPU with at least four cores. 
* 16 GB of RAM minimum. 
* Swapping disabled (recommended). 
* 2 GB of available hard disk space for installation and basic operation, additional disk space is required for source images, logs, data caches, and manifest files. 
* Fast Ethernet Network Interface Card.

**Note (Linux&reg;):** Image Serving does not work with SELinux turned on. This option is enabled by default. To disable SELinux, edit the [!DNL /etc/selinux/config] file and change the SELinux value from:

`SELINUX=enforcing`

To

`SELINUX=disabled`

**Note (Linux&reg;):** Make sure that the host name of the server is resolvable to an IP address. If that is not possible, add the fully qualified host name and the IP address to [!DNL /etc/hosts] as in the following example.

`<ip address> <fully qualified hostname>`

## Server software {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Dynamic Media Image Serving requires the following server software.

**Windows**

* Microsoft&reg; Windows Server 2008. 
* 64-bit operating system.

**Linux&reg;**

* Red Hat&reg; Enterprise 5 or CentOS 5.5 and later, with the latest fix patches. 
* 64-bit operating system.

**Note:** To use Image Serving on Windows, you must install the Microsoft&reg; Visual Studio 2010.
