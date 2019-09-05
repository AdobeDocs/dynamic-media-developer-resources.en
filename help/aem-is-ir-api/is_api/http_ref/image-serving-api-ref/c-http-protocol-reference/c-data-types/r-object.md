---
description: Source Object Specifier. Image, SVG, and ICC profile objects may be specified as image catalog entries or relative file paths
seo-description: Source Object Specifier. Image, SVG, and ICC profile objects may be specified as image catalog entries or relative file paths
seo-title: object
solution: Experience Manager
title: object
topic: Scene7 Image Serving - Image Rendering API
uuid: 25e92344-13ce-468e-bf7e-2aa8fd0c6c1a
index: y
internal: n
snippet: y
---

# object{#object}

Source Object Specifier. Image, SVG, and ICC profile objects may be specified as image catalog entries or relative file paths

 ` *`object`*[/]{[ *`rootId`*/] *`objId`*}| *`path`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId </span> </span> </p> </td> 
  <td class="stentry"> <p>name of the image catalog ( <span class="codeph"> attribute::RootId </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objtId </span> </span> </p> </td> 
  <td class="stentry"> <p>id of the image, SVG, template, or ICC profile record in the specified, main, or default image catalog </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> path </span> </span> </p> </td> 
  <td class="stentry"> <p>relative image, mask, or ICC profile file path and name </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> object </span> </span> </p> </td> 
  <td class="stentry"> <p>may occur either in the main URL path, or in a <span class="codeph"> src= </span>, <span class="codeph"> mask= </span>, or <span class="codeph"> icc= </span> command </p> </td> 
 </tr> 
</table>

*`rootId`* identifies an image catalog. (See [Image Catalog](../../../../../is_api/image_catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) for details.) If *`rootId`* is specified in the URL path, that catalog becomes the *main catalog* for this request. Otherwise the default catalog is used as the main catalog. Multiple different image catalogs can be used in the same request.

The server initially assumes that *`rootId`* is omitted in `src=`, `mask=`, and `icc=` commands and will attempt to find a catalog entry in the main catalog. Effectively, the server tries to use the entire *`object`* string as *`objId.`*

If a catalog entry is found, it is used; otherwise, the server next attempts to match the *`rootId`* of an image catalog. If a catalog is identified, it is searched for *`objId`*. If and entry is found, it is used.

Otherwise, *`object`* is assumed to be an explicit file path. In this case, if `attribute::FullMatch` is set in the main catalog, then the catalog is ignored for this object, and the default catalog used instead. If `attribute::FullMatch` is not set, then the main catalog is used for further processing.

Both *`rootId`* and *`objId`* are case-sensitive. *`path`* is case-sensitive on UNIX only.

If a leading '/' is specified, the default catalog will be searched instead of the main catalog. This is primarily useful when an explicit path requires `default::RootPath` rather than the main catalog's `attribute::RootPath`, but can also be used to gain access to entries in the default catalog which would otherwise be overridden by entries in the main catalog.

Refer to *Managing Content* in the *Server Configuration Guide* for details on how *`path`* is translated to a physical file path.

>[!NOTE]
>
>Comma ',' characters are not permitted in *`object.`*

## Supported image file formats {#section-12c85aead78e4f759856ca9ff10637d7}

Refer to the description of the IC (Image Converter) utility for a complete list of supported file formats.

Applications which require image data in multiple different resolutions will perform best when using the Scene7 pyramid TIFF (PTIF) multi-resolution format. The IC utility is used to create PTIF images from any supported image format.

## Examples {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**Accessing an image and an ICC profile in two different image catalogs**

Retrieve the image ' [!DNL myImage]' in the image catalog identified as ' [!DNL myCatalog]' and attach the ICC profile ' [!DNL sRGB]' located in the image catalog named ' [!DNL myProfiles]':

` http:// *`server`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

Using a single image catalog with layering

**Build a simple composite image consisting of three layers, all retrieved from ' [!DNL myCatalog]':**

` http:// *`server`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**Accessing image files directly while still using a catalog to provide attributes**

Access [!DNL my/image/path/myImage.tif], using the default jpg attributes configured in `myImageCatalog`:

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## See also {#section-b6eccefad63f441d922699c4aba58fc9}

[IC Utility](../../../../../is_api/is_utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b), [src=](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [attribute::FullMatch](../../../../../is_api/image_catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7) 
