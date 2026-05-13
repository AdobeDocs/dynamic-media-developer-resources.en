---
title: Verifying the installation
description: After you install Dynamic Media Image Serving, you should verify the installation.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
TQID: 'https://experienceleague.adobe.com/2i1-Ncy7lyIbm8BHFZGVLNIDnZUOA9sr3tZ970WswL4'
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
# Verifying the installation {#verifying-the-installation}

After you install Dynamic Media Image Serving, you should verify the installation.

 The Image Server is installed as a Windows Service.

1. Open the Services Control Panel and check that `Dynamic Media Image Serving` is present with a status of `Started`.
1. Open an Internet browser on the same or a different host and check the default server responses:

   `http:// server:port /is/image`

[!DNL  http:// *[!DNL server:port]*/ir/render]

Check for the presence of " `imageServer.`" items in the response, which indicate that the Image Server is listening.

>Additional verification can be performed using the sample pages of the Documentation and Demo packages, if installed.
