---
title: Errors
description: If a request cannot be completed successfully, the server either returns an error image or an HTTP response status other than 200 together with an error message.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e45e3968-3659-470b-a88a-fe7ba73d8207
---
# Errors{#errors}

If a request cannot be completed successfully, the server either returns an error image or an HTTP response status other than 200 together with an error message.

The response status value depends on the type of the error; for most common errors, it is '403'. Error responses for non-image request types conform to the format specified with `req=`. (Might not be consistently implemented currently.)

The amount of detail included in the error message is configurable with `attribute::ErrorDetail`.

**Error images**

Image Serving can be configured to return error messages rendered into an image. See `attribute::ErrorImage` in the image catalog reference for details. If the error image is successfully generated, the HTTP response status is 200. If an error occurs when processing the error image, the standard HTTP error response and text message is returned to the client.

**See also**

[attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) , [attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
