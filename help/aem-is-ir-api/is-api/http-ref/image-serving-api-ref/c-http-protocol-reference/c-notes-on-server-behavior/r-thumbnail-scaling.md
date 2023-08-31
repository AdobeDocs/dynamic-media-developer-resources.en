---
title: Thumbnail scaling
description: Step 2 of the image layer transforms is modified as follows for thumbnails (that is, if req=tmb).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
---
# Thumbnail scaling{#thumbnail-scaling}

Step 2 of the image layer transforms is modified as follows for thumbnails (that is, if req=tmb).

* `2.` If `size=` is specified, fit the (cropped) image into the `size=` rect using thumbnail rules. If `size=` is not specified, scale based on `res=`, or, if `res=` is not specified, fit the (cropped) image into the canvas rect using the thumbnail rules outlined below.
