---
description: Image Rendering enforces a two Megapixel size limitation for non-pyramid vignettes.
solution: Experience Manager
title: Vignette size limitation
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
---

# Vignette size limitation{#vignette-size-limitation}

Image Rendering enforces a two Megapixel size limitation for non-pyramid vignettes.

Modify the value of `IrMaxNonPyrVignetteSize` in [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] if your application requires support for non-pyramid vignettes with an image area (width x height) larger than this limit.

>[!NOTE]
>
>`attribute::MaxPix` and `IS::MaxMessageSize` may also need to be adjusted to allow unusually large response image sizes. Refer to the Image Serving documentation for details.

