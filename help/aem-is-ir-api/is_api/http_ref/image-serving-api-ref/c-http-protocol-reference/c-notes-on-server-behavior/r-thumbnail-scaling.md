---
description: Step 2 of the image layer transforms is modified as follows for thumbnails (i.e. if req=tmb).
seo-description: Step 2 of the image layer transforms is modified as follows for thumbnails (i.e. if req=tmb).
seo-title: Thumbnail scaling
solution: Experience Manager
title: Thumbnail scaling
topic: Scene7 Image Serving - Image Rendering API
uuid: d3ff4c57-e674-4686-9e50-af4a216bfe32
index: y
internal: n
snippet: y
---

# Thumbnail scaling{#thumbnail-scaling}

Step 2 of the image layer transforms is modified as follows for thumbnails (i.e. if req=tmb).

* 2. If `size=` is specified, fit the (cropped) image into the `size=` rect using thumbnail rules. If `size=` is not specified, scale based on `res=`, or, if `res=` is not specified, fit the (cropped) image into the canvas rect using the thumbnail rules outlined below.

