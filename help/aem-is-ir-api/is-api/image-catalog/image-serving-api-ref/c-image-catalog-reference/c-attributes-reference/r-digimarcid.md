---
description: Digimarc user info. Specifies the user information for Digimarc embedding.
solution: Experience Manager
title: DigimarcId
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac09c8cd-cb68-4b70-b1b4-9d4ca0166c7f
TQID: 'https://experienceleague.adobe.com/2kkvN1RLEhbDEmN4cA6lE5nGe9d-T3qcdxgGqF7L3Ig'
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
# DigimarcId{#digimarcid}

Digimarc user info. Specifies the user information for Digimarc embedding.

## Properties {#section-1e11a36d9e0b4bf3858c4ab15fe7a272}

Five or six comma-separated integer numbers. The third and fourth numbers are no longer used:

`creator-id, creator-pin, durability [ , chroma ]`

The `creator-id` and `creator-pin` are provided by Digimarc when the service is purchased. The unused values should be left empty.

`durability` specifies the Digimarc watermark embedding strength. It may be 1, 2, 3, or 4, with 1 indicating weakest and 4 strongest durability.

Set `chroma` to 1 to encode the watermark into the image's chrominance data or to 0 (default) to encode it into the luminance. This setting is ignored when outputting grayscale images.

## Default {#section-d6ecb6e95a7b4232bd612834ea49e6bc}

Inherited from `default::DigimarcId` if not defined or if empty.

## Example {#section-8469ae1c27b4461da3d53fbabc32d3c5}

Specify a test Digimarc creator id with durability set to 4.

`DigimarcId= 404407,32,,,4`

## See also {#section-75d4d2afd1df4127b31b1a82f30079d8}

[catalog::DigimarcInfo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba)
