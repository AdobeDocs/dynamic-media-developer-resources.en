---
description: After you install Dynamic Media Image Serving, you should verify the installation.
solution: Experience Manager
title: Verifying the installation
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
---
# Verifying the installation{#verifying-the-installation}

After you install Dynamic Media Image Serving, you should verify the installation.

 The Image Server is installed as a Windows Service. 

1. Open the Services Control Panel and check that "Dynamic Media Image Serving" is present with a status of "Started."
1. Open an Internet browser on the same or a different host and check the default server responses:

   `http:// server:port /is/image`

[!DNL  http:// *[!DNL server:port]*/ir/render]

   Check for the presence of " `imageServer.`" items in the response, which indicate that the Image Server is listening. 
>Additional verification can be performed using the sample pages of the Documentation and Demo packages, if installed.
