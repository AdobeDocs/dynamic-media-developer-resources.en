---
description: After you install Image Serving on Linux, verify the installation.
seo-description: After you install Image Serving on Linux, verify the installation.
seo-title: Verifying the installation
solution: Experience Manager
title: Verifying the installation
topic: Scene7 Image Serving - Image Rendering API
uuid: 16bfdcc7-359e-4acd-b972-5562ad857f58
index: y
internal: n
snippet: y
---

# Verifying the installation{#verifying-the-installation}

After you install Image Serving on Linux, verify the installation.

The Image Server is installed as a Linux daemon.

**To verify the installation** 

1. Verify that Image Serving is configured to start automatically and that it is running:

   `> /sbin/service ImageServing status`

   >[!NOTE] {class="- topic/note "}
   >
   >You must have root permissions to run these scripts.

1. Open an Internet browser on the same or a different host and check the default server response(s):

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL  http:// *[!DNL server:port]*/ir/render]

   In the responses, check for the presence of items starting with " `imageServer.`", which indicate that the Platform Server could successfully communicate with the Image Server. 
>Additional verification can be performed using the sample pages of the Documentation and Demo packages, if installed. 

