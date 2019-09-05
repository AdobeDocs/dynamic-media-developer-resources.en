---
description: Default response image. Specifies the image or catalog entry to be used in case an image file cannot be found and defaultImage= is not specified in the request.
seo-description: Default response image. Specifies the image or catalog entry to be used in case an image file cannot be found and defaultImage= is not specified in the request.
seo-title: DefaultImage
solution: Experience Manager
title: DefaultImage
topic: Scene7 Image Serving - Image Rendering API
uuid: f4438b9c-6a65-40e8-9864-af1d0532f72c
index: y
internal: n
snippet: y
---

# DefaultImage{#defaultimage}

Default response image. Specifies the image or catalog entry to be used in case an image file cannot be found and defaultImage= is not specified in the request.

May be either a catalog entry (including a template) or a relative (to `attribute::RootPath`) or absolute image file path. Useful for substituting missing images with default images.

## Properties {#section-b6d8193827c34e5f948792aba8b8daaf}

Text string. If specified, must be either a valid `catalog::Id` value in this image catalog or a relative (to `attribute::RootPath`) or absolute path to an image file accessible by the Image Server.

## Restrictions {#section-5d8ea872f0b0415fbd3a83410bbcf512}

Foreign image sources are not covered by the default image mechanism; an error is returned if a foreign image source is not valid.

## Default {#section-d88bc8fc71bd413e8f70281d57e1ba1c}

Inherited from `default::DefaultImage` if not defined. If defined but empty, default image behavior is disabled, even if `default::DefaultImage` is defined.

## See also {#section-dc0fb4e72294442882b33a479fbc2b82}

[attribute::DefaultImageMode](../../../../../is_api/image_catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) , [defaultImage=](../../../../../is_api/image_catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [attribute::RootPath](../../../../../is_api/image_catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [catalog::Id](r_id_cat.md#reference_C3F3CE9AAAC4451796A846D6722383E5), [attribute::ErrorImage](../../../../../is_api/image_catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c), [attribute::DefaultExpiration](../../../../../is_api/image_catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf) 
