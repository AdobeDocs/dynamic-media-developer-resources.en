---
description: Be aware of these thumbnail rules.
seo-description: Be aware of these thumbnail rules.
seo-title: Thumbnail rules
solution: Experience Manager
title: Thumbnail rules
uuid: 7d04b923-e062-4764-9e48-99a7bba72d3f
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# Thumbnail rules{#thumbnail-rules}

Be aware of these thumbnail rules.

1. If `catalog::ThumbType=Crop`, then the (cropped) image is scaled to the smallest size possible while still covering the entire target rect. If `catalog::ThumbType=Fit`, then the (cropped) image is scaled to the largest size possible while still fitting the entire image into the target rect. If `catalog::ThumbType=Texture`, the (cropped) image is scaled to the ratio of `catalog::ThumbRes` to `catalog::Resolution`. 
1. Align the scaled image with the target rect based on `attribute::ThumbHorizAlign` and `attribute::ThumbVertAlign`. 
1. Crop the result to the target rect.

