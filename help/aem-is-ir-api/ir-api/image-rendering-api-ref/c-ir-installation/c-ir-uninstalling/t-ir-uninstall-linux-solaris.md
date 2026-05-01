---
title: Uninstalling on Linux® and Solaris™
description: Follow these instructions to uninstall Image Rendering on a Linux® or Solaris™ system.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
TQID: https://experienceleague.adobe.com/qAqSZwGWEB56-Q-gqFtHxL-4slHcwrtdtLTDs-P19-0
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
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

