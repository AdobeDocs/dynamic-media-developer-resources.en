---
title: Uninstalling on Linux® and Solaris™
description: Follow these instructions to uninstall Image Rendering on a Linux® or Solaris™ system.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
---
# Uninstalling on Linux® and Solaris™{#uninstalling-on-linux-and-solaris}

Follow these instructions to uninstall Image Rendering on a Linux® or Solaris™ system. There are two different methods you can use. Do one of the following:

## Method 1

1. Find [!DNL uninstall.sh].

   It is in the directory from which ImageRendering was installed. If this directory has been removed, the original install package must be uncompressed and untarred to extract [!DNL uninstall.sh]. 
1. Run [!DNL uninstall.sh] and follow the on-screen instructions.

## Method 2 

1. Stop ImageRendering with the following:

   ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`

1. Remove ImageRendering from your system. The command you use depends on your system. 
   * Linux®: `rpm -e ImageRendering`

   * Solaris™: `pkgrm ImageRendering`

1. Delete any directories or files that were not removed in step 2. 

