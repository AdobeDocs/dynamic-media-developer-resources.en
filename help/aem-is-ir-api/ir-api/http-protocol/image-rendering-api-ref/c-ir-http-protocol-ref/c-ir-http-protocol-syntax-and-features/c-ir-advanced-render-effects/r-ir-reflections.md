---
title: Reflections
description: Vignettes can be authored to include near-3D reflection data.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f67ede68-03c0-461f-a16d-a308f76fd24c
TQID: https://experienceleague.adobe.com/Oo8DC2EhDyXvE32mp0N0aRBP8lvYOoLuzC3lukREF2Q
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
# Reflections{#reflections}

Vignettes can be authored to include near-3D reflection data.

If so authored, the following material attributes are used to define the material's reflective surface properties: 

<table id="table_8769C726A17E412FB41F7CB87690B1FE"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Attribute </p> </th> 
   <th class="entry"> <p>Description </p> </th> 
   <th class="entry"> <p>Default </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca" type="reference" format="dita" scope="local"> <span class="codeph"> gloss=</span> </a> </p> </td> 
   <td> <p>Surface glossiness </p> </td> 
   <td> <p>From vignette </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a" type="reference" format="dita" scope="local"> <span class="codeph"> glossmap= </span> </a> </p> </td> 
   <td> <p>Gloss variation (gray-scale image) </p> </td> 
   <td> <p>None </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180" type="reference" format="dita" scope="local"> <span class="codeph"> rough= </span> </a> </p> </td> 
   <td> <p>Surface roughness </p> </td> 
   <td> <p>40% </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35" type="reference" format="dita" scope="local"> <span class="codeph"> type=</span> </a> </p> </td> 
   <td> <p>Material type </p> </td> 
   <td> <p>0 (unknown) </p> </td> 
  </tr> 
 </tbody> 
</table>

The renderer adjusts the range of the `gloss=` and `rough=` attribute according to `type=`. Some material types such as fabric are less reflective than material types such as stone or metal. Furthermore, the same amount of gloss specified for one often results in a different reflection effect than the other. The attribute `gloss=` and roughness have a fairly wide gamut if `type=` is not specified or is set to `0`.

`glossmap=` Used to control the glossiness of a material on a pixel-by-pixel basis.
