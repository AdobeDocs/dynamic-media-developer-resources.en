---
description: Image set data. Provides a mechanism to define sorted sets of images and control attributes used by the Scene7 viewers.
seo-description: Image set data. Provides a mechanism to define sorted sets of images and control attributes used by the Scene7 viewers.
seo-title: ImageSet
solution: Experience Manager
title: ImageSet
topic: Scene7 Image Serving - Image Rendering API
uuid: 6f700167-ce7d-43d2-a3b8-cda055c557db
index: y
internal: n
snippet: y
---

# ImageSet{#imageset}

Image set data. Provides a mechanism to define sorted sets of images and control attributes used by the Scene7 viewers.

An image set consists of a sorted, comma-separated list of items, with each item consisting of one or more sub-items (image ids, swatch ids, media file paths, labels, etc), separated by semi-colons and/or colons.

Curly braces '{ }' and parentheses '( )' may be used to delimit certain content (such as color values) or indicate nested sets. Braces or parentheses used this way must not be encoded and must always appear as matched pairs, otherwise a catalog parsing error will occur.

>[!NOTE]
>
>The following characters are used as set delimiters and must be HTTP-encoded when they appear in the set as part of id or string values: 
>
>* , 
>* ; 
>* : 
>* { 
>* } 
>* ( 
>* ) 
>

Refer to the Image Serving Viewers documentation for additional details regarding the structure and use of image sets.

The server returns the contents of this field without modification in response to a `req=imageset` request.

## Standard Sets {#section-5ecc8ffee7224668b63f601383665564}

The following set definitions are natively supported by Image Serving, and access with certain viewers involves server-side parsing, validation, and processing of the set. Each set type can be identified by specifying the corresponding value in `catalog::AssetType`.

**Basic Swatch Sets**

Each item in a basic swatch set consists of a reference to an image record and an optional separate reference to an image record used as a swatch. 

|  ` *`basicSwatchSet`*`  | ` *`swatchItem`*&#42;[',' *`swatchItem`*]`  |
|---|---|
|  ` *`swatchItem`*`  | ` *`imageId`*[';' *`swatch`*]`  |
|  ` *`swatch`*`  | ` *`swatchId`*|solidColorSpecifier`  |
|  ` *`imageId`*`  | IS image reference (catalog/id)  |
|  ` *`swatchId`*`  | IS image reference (catalog/id)  |
|  ` *`solidColorSpecifier`*`  | ` '{0x' *`rrggbb`* [ *`label`*]'}'`  |
|  ` *`rrggbb`*`  | Packed 6 digit hex RGB color value for solid color swatches  |
|  ` *`label`*`  | Optional text label for solid color swatches  |

** Hierarchical Swatch Sets**

Each item in a hierarchical swatch set can consist of a basic swatch item or a reference to a swatch set record (swatches are required for such items).

|  ` *`hierarchicalSwatchSet`*`  | ` *`hierarchicalSwatchItem`* &#42;[ ',' *`hierarchicalSwatchItem`* ]`  |
|---|---|
|  ` *`hierarchicalSwatchItem`*`  | ` *`swatchItem`* | { *`basicSwatchSetId`* ';' *`swatch`* }`  |
|  ` *`basicSwatchSetId`*`  | IS reference (catalog/id) to a catalog record defining a basic swatch set  |

**Basic Spin Sets**

A basic spin set consists of a simple list of image ids.

|  ` *`basicSpinSet`*`  | ` *`imageId`* &#42;[ ';' *`imageId`* ]`  |
|---|---|

**Two-Dimensional Spin Sets**

Each item in a two-dimensional spin set can consist of a simple image, a reference to a basic spin set, or an in-line basic spin set delimited by curly braces. Parentheses may be used instead of curly braces.

|  ` *`2dSpinItem`*`  | ` *`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]`  |
|---|---|
|  ` *`2dSpinItem`*`  | ` *`imageId`* | { '{' *`basicSpinSet`* '}' } | *`basicSpinSetId`*`  |
|  ` *`basicSpinSetId`*`  | IS reference (catalog/id) to a catalog record defining a basic spin set  |

**Page Sets**

Each item in a page set can consist of up to three page images separated with colons.

|  ` *`pageSet`*`  | ` *`pageItem`* &#42;[ , *`pageItem`* ]`  |
|---|---|
|  ` *`pageItem`*`  | ` *`imageId`* [ : *`imageId`* [ : *`imageId`* ] ]`  |

**Media Sets**

Each item in a media set can consist of an image, basic swatch set, hierarchical swatch set, basic spin set, two-dimensional spin set, page set, or video asset. Each media set item can also contain an optional swatch and type identifier.

|  ` *`mediaSet`*`  | ` *`item`* &#42;[ , *`item`* ]`  |
|---|---|
|  ` *`item`*`  | ` { *`videoItem`* | *`recutItem`* | *`imageItem`*}} | *`setItem`* } [ ; [ *`ID`* ] [ ; [ *`reserved`* ] ] ]`  |
|  ` *`videoItem`*`  | ` *`video`* ; *`swatchId`*`  |
|  ` *`recutItem`*`  | ` *`recut`* ; *`swatchId`*`  |
|  ` *`imageItem`*`  | ` *`imageId`* ; [ *`swatchId`* ]`  |
|  ` *`setItem`*`  | ` { *`setId`* | { '{' *`inlineSet`* '}' } } ; *`swatchId`*`  |
|  ` *`ID`*`  | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]`  |
|  ` *`swatchId`*`  | IS image id  |
|  ` *`video`*`  | Video/animation file path or static catalog id  |
|  ` *`recut`*`  | Recut definition XML file path or static catalog id  |
|  ` *`imageId`*`  | IS image id  |
|  ` *`setId`*`  | IS reference to image, spin, or ecatalog set  |
|  ` *`inlineSet`*`  | Inlined image, spin, or ecatalog set  |
|  ` *`reserved`*`  | Reserved for future use  |

**Video Sets**

A video set consists of a simple list of video ids where each id references an entry in the static content catalog.

|  ` *`videoSet`*`  | ` *`videoId`* &#42;[ , *`videoId`* ]`  |
|---|---|

## Properties {#section-17c731e5c46646aa90ac21f39bb693ca}

Text string. Comma-separated list of `catalog::Id` values, absolute Image Server file paths, or file paths relative to `attribute::RootPath`. The same image may be referenced more than once in the set. The defining catalog record may appear in the set at any location.

This field participates in text string localization. In addition to *`label`* strings (part of the *`solidColorSpecifier`*) all delimited fields are localized if they include at least one ' `^loc=…^`' localization token. Refer to [Text String Localization](r_text_string_localization.md#reference_CAE5F6CEA4764762852ACAAB3B7B3527) in the *HTTP Protocol Reference* for details.

## Default {#section-c3a60e360393478284f0f2d2da5b963b}

None.

## See Also {#section-4c99c44f99074aa0a4ed90ba183bbc25}

` [req=imageset](r_req.md#reference_907CDB4A97034DB7AD94695F25552E76)`, ` [attribute::RootPath](r_rootpath.md#reference_17D57E5967BE403B8408FA7214017494)`, [Object Id Translation](r_object_id_translation.md#reference_CF3E34E6CBB346D69DED9982BFDEF414), [Text String Localization](r_text_string_localization.md#reference_CAE5F6CEA4764762852ACAAB3B7B3527), Image Serving Viewers Documentation 
