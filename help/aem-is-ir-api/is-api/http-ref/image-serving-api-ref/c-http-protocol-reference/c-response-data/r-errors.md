---
description: If a request cannot be completed successfully, the server either returns an error image or an HTTP response status other than 200 together with an error message.
solution: Experience Manager
title: Errors
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9314782f-703b-4e9c-a026-62970d1c752f
TQID: https://experienceleague.adobe.com/-hLxptQkMUodR7CYTnR5laPYdjGk7auxb3iSHAy1S74
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

The response status value depends on the type of the error; for most common errors it is '403'. Error responses for non-image request types conform to the format specified with `req=`. (May not be consistently implemented at this time.)

The amount of detail included in the error message is configurable with `attribute::ErrorDetail`.

## Error images {#section-92e9b20b2507433daa96923abc95f777}

Image Serving can be configured to return error messages rendered into an image.

See [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c) in the image catalog reference for details.

If the error image is successfully generated, the HTTP response status is 200. If an error occurs when processing the error image, the standard HTTP error response and text message is returned to the client.

## Default image {#section-66bf25fe6b434081bfae96d38d9be25e}

Image Serving can be configured to substitute a missing image with a default image. The default image can be specified either with `attribute::DefaultImage` or the `defaultImage=` command.

## See also {#section-e261d7f224ca4546bb64bf8cb909db08}

[attribute::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561) , [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c), [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [defaultImage=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
