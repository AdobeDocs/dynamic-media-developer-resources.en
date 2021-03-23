---
description: Error response image. Image Serving normally returns an error status with a text message when an error occurs.
solution: Experience Manager
title: ErrorImage
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# ErrorImage{#errorimage}

Error response image. Image Serving normally returns an error status with a text message when an error occurs.

 `attribute::ErrorImage` allows configuring an image, catalog entry, or template to be returned in case of error.

>[!NOTE]
>
>Missing images can also be handled with `attribute::DefaultImage`.

An Image Serving template can be configured which might render the error message text into the response image. The following predefined variables can be included in the `$error.title` template, which is substituted with a short error description, and `$error.message`, which is substituted by a more detailed error description (the level of detail is configured with `attribute::ErrorDetail`).

HTTP status 200 is returned if the error image/template can be processed successfully. If an error occurs during this processing, the HTTP error status and a text message are returned.

## Properties {#section-f460c6c2dd1f46b29f9a79b093575f45}

Text string. If specified, must be a valid catalog::Id value in an image catalog or a relative (to `attribute::RootPath`) or absolute path to an image file accessible by the Image Server.

## Default {#section-2885f289e5714ddca665a6aee401967f}

Inherited from `default::ErrorImage` if not defined. If defined but empty, error image behavior is disabled, even if `default::ErrorImage` is defined, and an HTTP error status and text message is returned.

## Example {#section-c92090abe1d247529542a8dd4960c2e6}

To get response images with the error message rendered into the image, we must first define the template in the image catalog. In this case, we create an entry in our image catalog called `onError`, containing the following in `catalog::Modifier`:

`size=300,300&bgc=ffffff&text=$error.message$`

The template is registered with `attribute::ErrorImage`:

`ErrorImage=myCatalog/onError`

For this example, the text will be rendered using the default font, font color, and font size.

## See also {#section-bbf1f85fc0a34033bdda1dd3e4e0bbb6}

[attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494) , [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md), [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [attribute::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561) 
