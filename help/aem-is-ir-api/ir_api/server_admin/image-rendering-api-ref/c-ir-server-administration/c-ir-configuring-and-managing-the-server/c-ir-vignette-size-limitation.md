---
description: Image Rendering enforces a two Megapixel size limitation for non-pyramid vignettes.
seo-description: Image Rendering enforces a two Megapixel size limitation for non-pyramid vignettes.
seo-title: Vignette size limitation
solution: Experience Manager
title: Vignette size limitation
topic: Scene7 Image Serving - Image Rendering API
uuid: e4ed23c4-1db4-49b0-b7af-793915558a72
index: y
internal: n
snippet: y
---

# Vignette size limitation{#vignette-size-limitation}

Image Rendering enforces a two Megapixel size limitation for non-pyramid vignettes.

Modify the value of `IrMaxNonPyrVignetteSize` in [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] if your application requires support for non-pyramid vignettes with an image area (width x height) larger than this limit.

>[!NOTE] {class="- topic/note "}
>
>`attribute::MaxPix` and `IS::MaxMessageSize` may also need to be adjusted to allow unusually large response image sizes. Refer to the Image Serving documentation for details.

