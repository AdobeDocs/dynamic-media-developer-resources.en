---
description: The features and syntax of image catalogs are described in this section.
solution: Experience Manager
title: Image catalogs
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c83ad2-a932-4df2-92ff-ab34d4a5b1a7
---
# Image catalogs{#image-catalogs}

The features and syntax of image catalogs are described in this section.

Image catalogs offer the following features:

* Allow persistent association of images with certain metadata and modifier commands.

  Entries in image catalogs are referenced using a shortcut notation `*`rootId/objId`*`, where `*`rootId`*` identifies the image catalog and `*`objId`*` identifies a data record in the catalog. 
* Provide defaults for certain request attributes, such as the JPEG quality or whether a watermark is to be applied. 
* Manage fonts, ICC profiles, macro definitions, and request templates

Even if no specific image catalogs are defined, all features of image catalogs are available via the default catalog ( [!DNL default.ini]).

If `*`rootId`*` in the request's URL path matches `attribute::RootId` of a specific image catalog, that catalog will become the main catalog for this request. The main catalog provides the default attributes and settings for the entire request. If no match is found, the default catalog is used instead.

A catalog identified in a `src=` or `mask=` command provides the following catalog attributes and data to the current layer: 

<table id="table_D3FA66EA5D054745900DE5A120885AA8"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Attribute/Data</b> </th> 
   <th class="entry"> <b> Notes</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::DefaultExt</span> </p> </td> 
   <td> <p> the default extension for all image file paths in the current layer </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Expiration</span> </p> </td> 
   <td> <p> default for <span class="codeph"> catalog::Expiration</span> or expiration of the current layer if no catalog record is involved </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Icc*</span> </p> </td> 
   <td> <p> the working ICC color profile, render intent, and blackpoint compensation flag for the request and/or the current layer </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootPath</span> </p> </td> 
   <td> <p> used for all source file paths of the current layer </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Resolution</span> </p> </td> 
   <td> <p> default for <span class="codeph"> catalog::Resolution</span> only </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Anchor</span> </p> </td> 
   <td> <p> default for the <span class="codeph"> anchor=</span> value of the current layer </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Expiration</span> </p> </td> 
   <td> <p> the smallest expiration value of all layers is used as the time-to-live value of the reply image </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::IccProfile</span> </p> </td> 
   <td> <p> the source image color profile for the current layer </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Map</span> </p> </td> 
   <td> <p> the image map data for the current layer </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::MaskPath</span> </p> </td> 
   <td> <p> default for <span class="codeph"> mask=</span> for the current layer </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Modifier</span> </p> </td> 
   <td> <p> prefix commands for the current layer (each command in <span class="codeph"> catalog::Modifier</span> can be overridden by the same command in the URL, if specified for the same layer) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Path</span> </p> </td> 
   <td> <p> the source image file for the current layer </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::PostModifier</span> </p> </td> 
   <td> <p> postfix commands for the current layer (similar to <span class="codeph"> catalog::Modifier</span>, but commands in <span class="codeph"> catalog::PostModifier</span> override the same commands specified in the URL or in <span class="codeph"> catalog::Modifier</span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Resolution</span> </p> </td> 
   <td> <p> the object resolution of the current layer </p> </td> 
  </tr> 
 </tbody> 
</table>

Within the same layer, `src=` and `mask=` must reference the same image catalog (if any).

A catalog identified in an `icc=` command is used only to look up an entry from the catalog's ICC profile table. No other catalog attributes or data are involved.

If, `*`rootId`*` resolves to a catalog, and `*`objId`*` is matched with a `catalog::Id` in this catalog, then `*`rootId/objId`*` is effectively replaced by the catalog entry somewhat like this:

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## See also {#section-00e4f6b39cd14244bcce537a3f831259}

[Image Catalog Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
