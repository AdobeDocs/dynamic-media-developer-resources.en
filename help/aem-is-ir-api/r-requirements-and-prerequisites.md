---
description: Before using Scene7 Image Serving, make sure your system meets the system requirements.
seo-description: Before using Scene7 Image Serving, make sure your system meets the system requirements.
seo-title: System requirements and prerequisites
solution: Experience Manager
title: System requirements and prerequisites
topic: Scene7 Image Serving - Image Rendering API
uuid: 80196574-f5a2-4298-880a-cc36f90b6e21
---

# System requirements and prerequisites{#system-requirements-and-prerequisites}

Before using Scene7 Image Serving, make sure your system meets the system requirements.

## Server hardware {#section-f3c14a7bc1b745118602659628df779f}

Your server should meet the following hardware requirements.

>[!NOTE] {class="- topic/note "}
>
>Systems with processors featuring AMD64 and Intel® EM64T are typically configured as NUMA (Non-Uniform Memory Architecture) platforms. This means that the kernel constructs multiple memory nodes at boot-time rather than constructing a single memory node. The multiple node construct can result in memory exhaustion on one or more of the nodes before other nodes become exhausted. When memory exhaustion happens the kernel can decide to kill processes (for example, the Image Server or Platform Server) even though there is available memory. Therefore, Adobe Systems recommends that if you are running such a system you turn off NUMA. Use the `numa=off` start option to avoid the kernel stopping these processes.

**Windows**

* Intel Xeon® or AMD® Opteron CPU with at least 4 cores. 
* 16GB of RAM minimum. 
* Swap space equal to at least twice the amount of physical memory (RAM). 
* 2 GB of available hard disk space for installation and basic operation, additional disk space is required for source images, logs, data caches, and manifest files. 
* Fast Ethernet Network Interface Card.

**Linux**

* Intel Xeon® or AMD® Opteron CPU with at least 4 cores. 
* 16GB of RAM minimum. 
* Swapping disabled (recommended). 
* 2 GB of available hard disk space for installation and basic operation, additional disk space is required for source images, logs, data caches, and manifest files. 
* Fast Ethernet Network Interface Card.

**Note (Linux):** Image Serving does not work with SELinux turned on. This option is enabled by default. To disable SELinux, edit the [!DNL /etc/selinux/config] file and change the SELinux value from:

`SELINUX=enforcing`

to

`SELINUX=disabled`

**Note (Linux):** Make sure that the host name of the server is resolvable to an IP address. If that is not possible, add the fully qualified host name and the IP address to [!DNL /etc/hosts] as in the following example.

`<ip address> <fully qualified hostname>`

## Server software {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Scene7 Image Serving requires the following server software.

**Windows**

* Microsoft® Windows 2008 Server. 
* 64-bit operating system.

**Linux**

* Red Hat® Enterprise 5 or CentOS 5.5 and later, with latest fix patches. 
* 64-bit operating system.

**Note:** To use Image Serving on Windows, you must install the Microsoft Visual Studio 2010 redistributable. The redistributable is available at the following location:

[http://www.microsoft.com/en-us/download/details.aspx?id=13523](http://www.microsoft.com/en-us/download/details.aspx?id=13523)

