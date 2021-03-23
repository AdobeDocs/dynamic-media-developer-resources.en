---
description: Use these server settings to set image size limits.
solution: Experience Manager
title: Image size limits
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
---

# Image size limits{#image-size-limits}

Use these server settings to set image size limits.

## IS::MaxMessageSize - Response Size Limit {#section-bd942385d4d144cd904003695d72c85e}

Limits the size of data the Image Server is allowed to send to the Platform Server. Effectively, this limits the size of the encoded/compressed response image that Image Serving can return to the client via HTTP (Mbytes).

## IS::MaxRenderRgnPixels - Output Image Size Limit {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

Limits the size of images the Image Server can produce (excluding images saved to file). Integer value larger than 0 in millions of pixels. An error is returned if a render operation would exceed the size limit. Default is 16.

## IS::MaxSavePixels - Size Limit For Saving to Files {#section-d1547c4afa88467080ab08356f775e06}

Limits the size of images the Image Server will write to files with the `req=saveToFile` command. Integer value larger than 0 in millions of pixels. An error is returned if the file save operation would exceed that limit. Default is 100 million pixels.

## IS::MaxNonDsfSize - Size Limit For Non-PTIFF Input Images {#section-50de28a7158a436393cce5da0d1e4d46}

The maximum size (in Mpixels) of images which are not PTIFFs that the Image Server is allowed to open. Image Serving will return an error when an attempt is made to access a non-PTIFF image which is larger than this limit.

>[!NOTE]
>
>Setting this value too high may cause the Image Server to be starved of memory and result in failures, including crashes.

