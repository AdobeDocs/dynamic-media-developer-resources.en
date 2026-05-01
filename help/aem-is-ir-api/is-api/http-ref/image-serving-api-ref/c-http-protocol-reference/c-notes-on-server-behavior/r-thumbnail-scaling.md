---
title: Thumbnail scaling
description: Step 2 of the image layer transforms is modified as follows for thumbnails (that is, if req=tmb).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
TQID: https://experienceleague.adobe.com/LZdC-nbahVGfByP6lA-DjE5NNiUXHhX7wJ26yImSLnQ
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
# Thumbnail scaling{#thumbnail-scaling}

Step 2 of the image layer transforms is modified as follows for thumbnails (that is, if req=tmb).

* `2.` If `size=` is specified, fit the (cropped) image into the `size=` rect using thumbnail rules. If `size=` is not specified, scale based on `res=`, or, if `res=` is not specified, fit the (cropped) image into the canvas rect using the thumbnail rules outlined below.
