---
description: Cabinets materials specify a cabinet style file (.vnc file extension), a special data file containing photographic representations of cabinets together with parametric layout definitions and other information required for rendering cabinet fronts.
solution: Experience Manager
title: Cabinets
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cdb3ed5e-c396-483d-aea0-2b3f24efe56e
---
# Cabinets{#cabinets}

Cabinets materials specify a cabinet style file (.vnc file extension), a special data file containing photographic representations of cabinets together with parametric layout definitions and other information required for rendering cabinet fronts.

 [!DNL vnc] files may either include a repeatable wood grain texture, or the texture can be provided externally via a second argument to `src=`. Certain [!DNL vnc] files allow colorizing or texturing selected areas of cabinet fronts (typically used for laminate cabinet styles).

Cabinet materials can only be applied to cabinet objects.

<table id="table_0B16200886FE4DFEBB1E4BE8FBA67EE4"> 
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
   <td colname="col2"> <p>Cabinet style file; required. </p> </td> 
   <td colname="col3"> <p>None. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>Optional texture image file (second value for <span class="codeph"> src= </span>). </p> </td> 
   <td colname="col3"> <p>None. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>Optional texture resolution. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Resolution </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> color= </span> </a> </p> </td> 
   <td colname="col2"> <p>Colorizes cabinet and/or texture. </p> </td> 
   <td colname="col3"> <p>None. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span> </a> </p> </td> 
   <td colname="col2"> <p>Sharpening. </p> </td> 
   <td colname="col3"> <p>0 (no sharpening) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-flags.md#reference-3a4844f0f21346d79e6508aaad9a9ac9" type="reference" format="dita" scope="local"> <span class="codeph"> flags= </span> </a> </p> </td> 
   <td colname="col2"> <p>Special render flags. </p> </td> 
   <td colname="col3"> <p>0 (no flags) </p> </td> 
  </tr> 
 </tbody> 
</table>
