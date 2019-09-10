---
description: Progressive JPEG scan. Progressive JPEG displays an image in such a way that it initially shows a blurry/low-quality photo in its entirety. As the scanning passes continue, it becomes clearer as the image's data becomes more fully downloaded. This parameter lets you set the number of scans it takes (3, 4, or 5) for the entire image to appear.
seo-description: Progressive JPEG scan. Progressive JPEG displays an image in such a way that it initially shows a blurry/low-quality photo in its entirety. As the scanning passes continue, it becomes clearer as the image's data becomes more fully downloaded. This parameter lets you set the number of scans it takes (3, 4, or 5) for the entire image to appear.
seo-title: pscan
solution: Experience Manager
title: pscan
topic: Scene7 Image Serving - Image Rendering API
uuid: c8e1d7a9-679c-437f-aa53-67aca3f40b30
index: y
internal: n
snippet: y
---

# pscan{#pscan}

Progressive JPEG scan. Progressive JPEG displays an image in such a way that it initially shows a blurry/low-quality photo in its entirety. As the scanning passes continue, it becomes clearer as the image's data becomes more fully downloaded. This parameter lets you set the number of scans it takes (3, 4, or 5) for the entire image to appear.

 `pscan=auto|3|4|5`

The actual speed of each scan depends on the transmission speed of the user's system and the computer that receives and decompresses the data.

`Auto` uses the scan settings that are computed by the independent JPEG library and depends upon the color model. The values of `3`, `4`, `5` correspond to the Scan setting found in Adobe Photoshop when you save a JPEG file as a pjpeg (progressive JPEG).

If `pscan` is not set, it defaults to `auto`.

## Properties {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

Request attribute. Applies regardless of the current layer setting. Ignored if the output format is not progressive JPEG.

## Default {#section-01948f6cd7a2415091004cd7526436c7}

`pscan=auto`

## Example {#section-d51bc4d0e8a9473786f149cba9540506}

`http://localhost:8080/is/image/demo/bedroom.tif?wid=300&fmt=pjpeg&pscan=4`

## See also {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) 
