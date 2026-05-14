---
title: Verifying the installation
description: After you install Image Serving on Linux®, verify the installation.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 273478ab-f245-48ef-a125-fb738054484e
TQID: 'https://experienceleague.adobe.com/LyHlwiFL1b-iwo1kSnUeNfNo3fZY6FZetHgnNFoxGZo'
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
# Verifying the installation{#verifying-the-installation}

After you install Image Serving on Linux®, verify the installation.

The Image Server is installed as a Linux® daemon.

**To verify the installation** 

1. Verify that Image Serving is configured to start automatically and that it is running:

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >You must have root permissions to run these scripts.

1. Open an Internet browser on the same or a different host and check the default server responses:

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL  http:// *[!DNL server:port]*/ir/render]

   In the responses, check for the presence of items starting with `imageServer`, which indicate that the [!DNL Platform Server] could successfully communicate with the Image Server.

>Additional verification can be performed using the sample pages of the Documentation and Demo packages, if installed.
