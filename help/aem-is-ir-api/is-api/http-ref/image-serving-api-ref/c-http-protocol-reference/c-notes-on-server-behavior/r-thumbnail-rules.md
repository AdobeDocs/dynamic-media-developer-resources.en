---
description: Be aware of these thumbnail rules.
solution: Experience Manager
title: Thumbnail rules
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d81dc4ad-dd59-4235-996e-58996f009d88
TQID: 'https://experienceleague.adobe.com/2HjWzEcMFnTFzwDWz-Ld7wZ6FsFcq3gwaUFcSWgxPko'
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
# Thumbnail rules{#thumbnail-rules}

Be aware of these thumbnail rules.

1. If `catalog::ThumbType=Crop`, then the (cropped) image is scaled to the smallest size possible while still covering the entire target rect. If `catalog::ThumbType=Fit`, then the (cropped) image is scaled to the largest size possible while still fitting the entire image into the target rect. If `catalog::ThumbType=Texture`, the (cropped) image is scaled to the ratio of `catalog::ThumbRes` to `catalog::Resolution`. 
1. Align the scaled image with the target rect based on `attribute::ThumbHorizAlign` and `attribute::ThumbVertAlign`. 
1. Crop the result to the target rect.
