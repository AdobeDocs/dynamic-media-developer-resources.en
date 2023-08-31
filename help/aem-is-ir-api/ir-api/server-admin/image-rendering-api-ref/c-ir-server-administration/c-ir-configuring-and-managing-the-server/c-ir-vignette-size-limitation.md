---
title: Vignette size limitation
description: Image Rendering enforces a two-megapixel size limitation for non-pyramid vignettes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
---
# Vignette size limitation{#vignette-size-limitation}

Image Rendering enforces a two-megapixel size limitation for non-pyramid vignettes.

Modify the value of `IrMaxNonPyrVignetteSize` in [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] if your application requires support for non-pyramid vignettes with an image area (width x height) larger than this limit.

>[!NOTE]
>
>Adjust the attributes `attribute::MaxPix` and `IS::MaxMessageSize` to allow unusually large response image sizes. Refer to the Image Serving documentation for details.
