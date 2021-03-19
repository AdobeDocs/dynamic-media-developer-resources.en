---
description: Material file. Specifies material data, either in form of a single material catalog reference, or as one or two image or material data files, separated with a comma.
seo-description: Material file. Specifies material data, either in form of a single material catalog reference, or as one or two image or material data files, separated with a comma.
seo-title: src
solution: Experience Manager
title: src
uuid: 52751bcc-a65d-4441-a3b5-802d27b54b54
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# src{#src}

Material file. Specifies material data, either in form of a single material catalog reference, or as one or two image or material data files, separated with a comma.

 `src = *`catalogEntry`*|{{ *`materialFile`*| *`embeddedReq`*}[, *`materialFile`*]`

`srcE= *`name`*`

`srcN= *`index`*`

<table id="simpletable_A64C4F084C0A4DDCA45A921D4BD7AAEA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catalogEntry</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">[/][<span class="varname"> catId</span>/]<span class="varname"> recId</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> materialFile</span> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> styleFile</span>|<span class="varname"> imageFile</span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> embeddedReq</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">&lbrace;'is&lbrace;'<span class="varname"> isReq</span>'&rbrace;'&rbrace;|&lbrace;'ir&lbrace;'<span class="varname"> irReq</span>'&rbrace;'|&lbrace;'&lbrace;'<span class="varname"> foreignReq</span>'&rbrace;'</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p></td> 
  <td class="stentry"> <p>Material catalog ID (<span class="codeph"> attribute::RootId</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>Material catalog entry (<span class="codeph"> catalog::Id</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> styleFile</span> </p></td> 
  <td class="stentry"> <p>Material style file (<span class="filepath"> .vnc</span> or <span class="filepath"> .vnw</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> imageFile</span> </p></td> 
  <td class="stentry"> <p>Image data file. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> isReq</span> </p></td> 
  <td class="stentry"> <p>Request to Image Serving. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> irReq</span> </p></td> 
  <td class="stentry"> <p>Request to Image Rendering. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> foreignReq</span> </p></td> 
  <td class="stentry"> <p>Request to a foreign server. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p></td> 
  <td class="stentry"> <p>Name of an embedded material. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> index</span> </p></td> 
  <td class="stentry"> <p>0-based index number for an embedded material. </p></td> 
 </tr> 
</table>

Repeatable Texture, Decal, and Wallpaper materials require a single image, which may be specified as a file or an embedded request.

Cabinet materials require a cabinet style file ( [!DNL .vnc]), which cannot be specified as a nested request. A texture image file is optional for cabinets, and, if specified, it may be either a file or an embedded request.

Window coverings materials require a window coverings style file ( [!DNL .vnw]), which cannot be specified as a nested request. A texture file is optional and, if specified, it may be either a file or an embedded request.

Image Rendering uses the same rules as Image Serving for looking up material catalogs, catalog entries, and data files. Refer to the description of the *`object`* Data Type in the Image Serving documentation for details.

*`materialFile`* is a path relative to `attribute::RootPath`.

*`foreignReq`* can either be a URL relative to `attribute::RootUrl`, or an absolute URL if `attribute::AllowDirectUrls` is set.

If *`catId`* is not specified, the session catalog is used.

`srcE=` and `srcN=` provide access to materials embedded in the vignette.

## Supported file formats {#section-f2186d3eef834fc8bbecb2bc68daacad}

Image Rendering supports the same source image formats as Dynamic Media Image Serving.

Applications which require image data in multiple different resolutions will perform best when using the Scene7 pyramid TIFF (PTIFF) multi-resolution format. Image Serving includes the Image Converter (IC) utility which creates PTIFF images from any supported format.

Refer to the description of the IC utility in the Image Serving documentation for a complete list of supported file formats.

## Properties {#section-e68d03788d534e2184147987d51dfd0f}

Material attribute. Required for all materials except solid color (not permitted for solid color materials). All strings are case-sensitive. *`index`* must be 0 or larger.

## Default {#section-dde549c1917540dc8f9555962202da3c}

None.

## Example {#section-675865444f8a4d35b9fc6e58b36e3438}

A MSS for a colorized cabinet with a separate repeatable texture:

`…&obj=cabinets&src=cabs/maple02.vnc,cabs/maple.jpg&res=40&color=185,105,35&…`

The same material could be located in a material catalog `'cat`' in record ' `12-3-2`':

`…&obj=cabinets&src=cat/12-3-2&…`

A nested request to Image Serving to obtain a texture image:

`…&obj=main&src=is{texCatalog/texture123?res=30}&res=30&…`

## See also {#section-d01d25b8903e4f5ca6aef4a084fca6b7}

[Material Catalogs](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2), [attribute::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402), [attribute::AllowDirectUrls](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-allowdirecturls.md#reference-02000c0f3c494292bad8425d06268882) 
