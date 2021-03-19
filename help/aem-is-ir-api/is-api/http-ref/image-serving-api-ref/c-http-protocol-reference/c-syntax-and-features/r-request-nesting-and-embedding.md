---
description: Image Serving supports unlimited nesting of Image Serving requests, embedding of Image Rendering requests, as well as embedding images retrieved from foreign servers. Only layer images and layer masks support these mechanisms.
seo-description: Image Serving supports unlimited nesting of Image Serving requests, embedding of Image Rendering requests, as well as embedding images retrieved from foreign servers. Only layer images and layer masks support these mechanisms.
seo-title: Request nesting and embedding
solution: Experience Manager
title: Request nesting and embedding
uuid: 59031329-e65f-4631-bc7d-83f2540cc836
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# Request nesting and embedding{#request-nesting-and-embedding}

Image Serving supports unlimited nesting of Image Serving requests, embedding of Image Rendering requests, as well as embedding images retrieved from foreign servers. Only layer images and layer masks support these mechanisms.

>[!NOTE]
>
>Certain email clients and proxy servers may encode the curly braces used for the nesting and embedding syntax. Applications for which this is an issue should use parentheses instead of curly braces.

## Nested Image Serving requests {#section-6954202119e0466f8ff27c79f4f039c8}

An entire Image Serving request can be used as a layer source by specifying it in the `src=` (or `mask=`) command using the following syntax:

`…&src=is( nestedRequest)&…`

The `is` token is case-sensitive.

The nested request must not include the server root path (typically ` http:// *[!DNL server]*/is/image/'`).

>[!NOTE]
>
>The nested request delimiter characters ( `'(',')'`) and the command delimiter characters ( `'?'`, `'&'`, `'='`) within nested requests must not be HTTP-encoded. Effectively, nested requests must be encoded the same as the outer (nesting) request.

Preprocessing rules are applied to nested requests.

The following commands are ignored when specified in nested requests (either in the request URL or in `catalog::Modifier` or `catalog::PostModifier`):

* `fmt=` 
* `qlt=` 
* `iccEmbed=` 
* `printRes=` 
* `quantize=` 
* `req=` 
* `bgc=`

If the result image of the nested requests includes mask (alpha) data, it is passed to the embedding layer as the layer mask.

Also ignored are `attribute::MaxPix`and `attribute::DefaultPix` of the image catalog that applies to the nested request.

The image result of a nested IS request can be cached optionally by including `cache=on`. By default, caching of intermediate data is disabled. Caching should be enabled only when the intermediate image is expected to be reused in a different request within a reasonable time period. Standard server-side cache management applies. Data is cached in a lossless format.

## Embedded Image Render requests {#section-69c5548db930412b9b90d9b2951a6969}

When Dynamic Media Image Rendering is enabled on the server, render requests can be used as layer sources by specifying them in src= (or mask=) command. Use the following syntax:

` …&src=ir( *[!DNL renderRequest]*)&…`

The `ir` token is case-sensitive.

*[!DNL renderRequest]* is the usual Image Rendering request, excluding the HTTP root path ` http:// *[!DNL server]*/ir/render/`.

>[!NOTE]
>
>The nested request delimiter characters ( `'(',')'`) and the command delimiter characters ( `'?'`, `'&'`, `'='`) within nested requests must not be HTTP-encoded. Effectively, embedded requests must be encoded the same as the outer (embedding) request.

The following Image Rendering commands are ignored when specified in nested requests:

* `fmt=` 
* `qlt=` 
* `icc=` 
* `iccEmbed=` 
* `printRes=` 
* `req=`

Also ignored are `attribute::MaxPix` and `attribute::DefaultPix` of the material catalog that applies to the nested render request.

The image result of a nested IR request can be cached optionally by including `cache=on`. By default, caching of intermediate data is disabled. Caching should be enabled only when the intermediate image is expected to be reused in a different request within a reasonable time period. Standard server-side cache management applies. Data is cached in a lossless format.

## Embedded FXG render requests {#section-c817e4b4f7da414ea5a51252ca7e120a}

When the FXG graphics renderer (aka [!DNL AGMServer]) is installed and enabled with Image Serving, FXG requests can be used as layer sources by specifying them in `src=` (or `mask=`) commands. Use the following syntax:

`…&src=fxg( renderRequest)&…`

The `fxg` token is case-sensitive.

>[!NOTE]
>
>FXG graphics rendering is available only in the Dynamic Media hosted environment and may require additional licensing. Contact Dynamic Media technical support for more information.

*[!DNL renderRequest]* is the usual FXG render request, excluding the HTTP root path ` http:// *[!DNL server]*/agm/render/`.

>[!NOTE]
>
>The delimiter characters ( `'(',')'`) and the command delimiter characters ( `'?'`, `'&'`, `'='`) within nested requests must not be HTTP-encoded. Effectively, embedded requests must be encoded the same as the outer (embedding) request.

The following FXG commands are ignored when specified in nested requests:

* `fmt=` 
* `qlt=` 
* `icc=` 
* `iccEmbed=` 
* `cache=`

## Foreign image sources {#section-84e83ecfcd1a43748cdfc7a6f8c04cb8}

Image Serving supports access to source images on foreign HTTP servers.

>[!NOTE]
>
>Only the HTTP protocol is supported for remote URLs.

To specify a foreign URL for a `src=` or a `mask=` command, delimit the foreign URL or URL fragment with parentheses:

`…&src=( foreignUrl)&…`

Important The delimiter characters ( `'(',')'`) and the command delimiter characters ( `'?'`, `'&'`, `'='`) within nested requests must not be HTTP-encoded. Effectively, embedded requests must be encoded the same as the outer (embedding) request.

Full absolute URLs (if `attribute::AllowDirectUrls` is set), and URLs relative to `attribute::RootUrl` are permitted. An error occurs if an absolute URL is embedded and attribute:: `AllowDirectUrls` is 0, or if a relative URL is specified and `attribute::RootUrl` is empty.

While foreign URLs cannot be specified directly in the path component of the request URL, it is possible to set up a preprocessing rule to permit conversion of relative paths to absolute URLs (see the example below).

Foreign images are cached by the server according to the caching headers included with the HTTP response. If neither an `ETag` nor a Last-Modified HTTP response header is present, the response is not cached. This can cause poor performance for repeat accesses for the same foreign image, as Image Serving needs to re-fetch and revalidate the image on every access.

This mechanism supports the same image file formats which are supported by the Image Convert (IC) utility, with the exception of source images with 16 bits per component.

>[!NOTE]
>
>Image Serving will automatically run the validate utility when a foreign image is first used, to ensure that the image is valid and has not been corrupted during transmission. This may cause a slight delay on first access. For best performance, it is recommended to limit the size of such images and/or use an image file format that compresses well.

## Restrictions {#section-fb68e3f0d40947feb94d7bf183b64929}

The size of the image generated by nested/embedded requests is normally optimized automatically. If caching of nested request images is enabled, incremental performance gains may be achieved by specifying the exact size of the nested image, so that no further scaling is required when the cache entry is reused.

Important Image Serving does not support double-encoding of nested or embedded requests. Nested and embedded requests must be HTTP-encoded just like simple requests.

## Examples {#section-d800cfc31abe46d2a964f8e7929231f1}

**Layering template with caching:**

Use nesting to add caching to a layering template. A limited number of background images are overlaid with highly variable text. The initial template string might look like this:

`layer=0&src=$img$&size=300,300&layer=1&text=$txt$`

With slight modifications, we can pre-scale the layer 0 image and cache it persistently, thereby reducing server load:

`layer=0&src=is(?src=$img$&size=300,300&cache=on)&layer=1&text=$txt$`

**Embedding requests for Dynamic Media Image Rendering**

Using a template stored in [!DNL myCatalog/myTemplate]; generate the image for layer2 of the template using Dynamic Media Image Rendering:

`http://server/is/image/myCatalog/myTemplate?layer=2&src=ir(myRenderCatalog/myRenderObject?id=myIdValue&sel=group&src=is(myCatalog/myTexture1?res=30)&res=30)&wid=300`

Note the nested curly braces. The Image Rendering request embeds a call back to Image Serving to retrieve a repeatable texture.

## See also {#section-109a0a9a3b144158958351139c8b8e69}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [Request PreProcessing](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-preprocessing.md#reference-c27976436bf04194bfbe9adf40ea98e3), Image Rendering Reference, [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [Image Serving Utilities](../../../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f) 
