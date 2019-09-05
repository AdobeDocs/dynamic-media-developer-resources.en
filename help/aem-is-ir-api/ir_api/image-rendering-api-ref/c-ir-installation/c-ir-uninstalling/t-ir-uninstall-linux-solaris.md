---
description: Follow these instructions to uninstall Image Rendering on a Linux or Solaris system.
seo-description: Follow these instructions to uninstall Image Rendering on a Linux or Solaris system.
seo-title: Uninstalling on Linux and Solaris
solution: Experience Manager
title: Uninstalling on Linux and Solaris
topic: Scene7 Image Serving - Image Rendering API
uuid: f5d3c200-2cd1-4f71-b017-b27b79857c4b
index: y
internal: n
snippet: y
---

# Uninstalling on Linux and Solaris{#uninstalling-on-linux-and-solaris}

Follow these instructions to uninstall Image Rendering on a Linux or Solaris system.

There are two ways to uninstall Image Rendering on a Linux or Solaris system.

**Method 1** 

1. Find [!DNL uninstall.sh].

   It is located in the directory from which ImageRendering was installed from. If this directory has been removed, the original install package must be uncompressed and untarred to extract [!DNL uninstall.sh]. 
1. Run [!DNL uninstall.sh] and follow the instructions on the screen.
>**Method 2** 
>
>1. Stop ImageRendering with: ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`
>1. Remove ImageRendering from your system. 
>
>   The command to remove ImageRendering depends on your system: 
>
>   Linux: `rpm -e ImageRendering`
>
>   Solaris: `pkgrm ImageRendering`
>
>1. Delete any directories or files that were not removed in Step 2. 
>

