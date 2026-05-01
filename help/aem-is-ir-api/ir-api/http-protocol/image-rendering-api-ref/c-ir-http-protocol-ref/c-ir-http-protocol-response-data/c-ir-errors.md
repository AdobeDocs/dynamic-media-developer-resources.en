---
title: Errors
description: If a request cannot be completed successfully, the server either returns an error image or an HTTP response status other than 200 together with an error message.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e45e3968-3659-470b-a88a-fe7ba73d8207
TQID: https://experienceleague.adobe.com/OjKJS9g23o4BjWzuO7EJl1LCCtgdfdXVr0yTYtTr0JQ
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
# Errors{#errors}

If a request cannot be completed successfully, the server either returns an error image or an HTTP response status other than 200 together with an error message.

The response status value depends on the type of the error; for most common errors, it is '403'. Error responses for non-image request types conform to the format specified with `req=`. (Might not be consistently implemented currently.)

The amount of detail included in the error message is configurable with `attribute::ErrorDetail`.

**Error images**

Image Serving can be configured to return error messages rendered into an image. See `attribute::ErrorImage` in the image catalog reference for details. If the error image is successfully generated, the HTTP response status is 200. If an error occurs when processing the error image, the standard HTTP error response and text message is returned to the client.

**See also**

[attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) , [attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
