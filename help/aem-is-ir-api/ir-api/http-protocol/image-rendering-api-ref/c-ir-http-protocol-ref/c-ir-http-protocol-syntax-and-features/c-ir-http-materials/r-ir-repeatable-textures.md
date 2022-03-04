---
title: Repeatable textures
description: Repeatable textures include interior and exterior materials, such as fabrics (both apparel and upholstery), wall-to-wall floor coverings, wallpapers, countertop materials, wood grain textures, roofing and siding materials, and any other generic texture.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3693498b-994a-460a-8b2e-780a1482d37a
---
# Repeatable textures{#repeatable-textures}

Repeatable textures include interior and exterior materials, such as fabrics (both apparel and upholstery), wall-to-wall floor coverings, wallpapers, countertop materials, wood grain textures, roofing and siding materials, and any other generic texture.

Repeatable textures can be applied to flat, flowline, sketch, plane, wall, and cabinet objects. When applied to a non-texturable object, the object is painted with `color=` (or `bgc=` if `color=` is not specified).

A material is considered a texture if it includes a `src=` attribute specifying an image and if it occurs in an MSS other than decal or wall border.

When rendering, the texture is aligned with the object by matching the `anchor=` point of the texture material with the texture origin point of the object (as authored in the vignette).

<table id="table_992A6E93E4274B598A236F8F728F017A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Attribute </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
   <th colname="col3" class="entry"> <p>Default </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>Repeatable texture image; required </p> </td> 
   <td colname="col3"> <p>None. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>Texture resolution </p> </td> 
   <td colname="col3"> <span class="codeph"> attribute::Resolution </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> anchor= </span> </a> </p> </td> 
   <td colname="col2"> <p>Texture alignment point </p> </td> 
   <td colname="col3"> <p>Top-left corner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> repeat= </span> </a> </p> </td> 
   <td colname="col2"> <p>Repeat mode </p> </td> 
   <td colname="col3"> <p>0 (straight repeat). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span> </a> </p> </td> 
   <td colname="col2"> <p>Sharpening </p> </td> 
   <td colname="col3"> <p>0 (no sharpening). </p> </td> 
  </tr> 
 </tbody> 
</table>

In addition to these basic attributes, repeatable textures support the following special-purpose attributes for advanced applications:

<table id="table_A97365804CB143DEB31F26A65DA3CE04"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Attribute </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
   <th colname="col3" class="entry"> <p>Default </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a" type="reference" format="dita" scope="local"> <span class="codeph"> grout= </span> </a> </p> </td> 
   <td colname="col2"> <p>Grout color and thickness; useful for ceramic/stone tile materials </p> </td> 
   <td colname="col3"> <p>Grout already present in image </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7" type="reference" format="dita" scope="local"> <span class="codeph"> align= </span> </a> </p> </td> 
   <td colname="col2"> <p>Alignment mode (between objects); used for upholstery applications </p> </td> 
   <td colname="col3"> <p>Center-matched </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rotate.md#reference-3745d74a913e4065b7ac009fb4fd9e3c" type="reference" format="dita" scope="local"> <span class="codeph"> rotate= </span> </a> </p> </td> 
   <td colname="col2"> <p>Texture rotation angle; not supported by wall objects </p> </td> 
   <td colname="col3"> <p>0 (no rotation) </p> </td> 
  </tr> 
 </tbody> 
</table>
