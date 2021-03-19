---
description: Step 2 of the image layer transforms is modified as follows for thumbnails (i.e. if req=tmb).
seo-description: Step 2 of the image layer transforms is modified as follows for thumbnails (i.e. if req=tmb).
seo-title: Thumbnail scaling
solution: Experience Manager
title: Thumbnail scaling
uuid: df935d40-84c6-4018-9e41-faef4653ff1f
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# Thumbnail scaling{#thumbnail-scaling}

Step 2 of the image layer transforms is modified as follows for thumbnails (i.e. if req=tmb).

* `2.` If `size=` is specified, fit the (cropped) image into the `size=` rect using thumbnail rules. If `size=` is not specified, scale based on `res=`, or, if `res=` is not specified, fit the (cropped) image into the canvas rect using the thumbnail rules outlined below.

