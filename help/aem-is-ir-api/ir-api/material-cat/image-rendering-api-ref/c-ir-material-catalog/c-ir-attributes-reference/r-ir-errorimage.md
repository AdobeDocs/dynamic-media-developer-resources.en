---
title: ErrorImage
description: Error response image. Image Rendering normally returns an error status with a text message when an error occurs.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ed48482f-79b0-4c81-b5cd-cf997f27d3ab
---
# ErrorImage {#errorimage}

Error response image. Image Rendering normally returns an error status with a text message when an error occurs. The `attribute::ErrorImage` allows configuring an image to be returned if there is an error.

When an error occurs, the server attempts to interpret the value of `ImageRendering::attribute::ErrorImage`as a simple image file path. If the file cannot be opened, it sends the attribute value and error details to Image Serving, which processes as described in `ImageServing::attribute::ErrorImage`. If Image Serving does not return a valid response image, the standard HTTP error status and text message are sent to the client.

Error images are returned with HTTP status 200.

## Properties {#section-4a4a7e37ed11483db0b9922dc68ea7db}

Text string. If specified, it must either be an **`ImageServing::catalog::id`** value, a relative path (to **`ImageServing::attribute::RootPath`** or **`ImageRendering::attribute::RootPath`**), or an absolute path to an image file that is accessible by the Image Server.

## Default {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

Inherited from `default::ErrorImage` if it is not defined. If it is defined but empty, error image behavior is disabled, even if `default::ErrorImage` is defined, and an HTTP error status is returned.

## See also {#section-3e0308eaf4124451909dacd570e27695}

[attribute::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f), [attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3), [catalog::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
