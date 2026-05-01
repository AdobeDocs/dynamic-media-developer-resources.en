---
title: rough
description: Material surface roughness. Specifies the relative roughness of the material surface.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8903b51c-c7d4-460f-8f28-00053eac9d6e
TQID: https://experienceleague.adobe.com/kZ6zEbEvCWOgjB3GWDePdh-vD1rIDlsLl5J8gx4geCg
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
# rough{#rough}

Material surface roughness. Specifies the relative roughness of the material surface.

 ` rough= *`val`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Surface roughness (0…100 percent) or -1 to select the default roughness. </p> </td> 
 </tr> 
</table>

Used to control the 3D reflection render effect. Lower roughness values typically produce smoother reflection effects; higher values cause randomization and scattering of the reflected image.

Each material type ( `type=`) defines a minimum and a maximum reflection render effect based on roughness. For some material types (for example, wall paper), `rough=` has minimal any impact on the appearance of the reflection, while for other material types (for example, stone or ceramic), the effect is substantially more pronounced.

`rough=-1` Sets the roughness to a server-internal default value (40% for typical material types).

## Properties {#section-515375758b254c80af576271bdb61bb8}

Material attribute. Ignored if the vignette has no 3D reflection capability, if the target object does not have 3D geometry associated with it, or if the target object is not reflecting any other objects in the scene.

## Default {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` If the material is based on a catalog entry, otherwise approximately 40%.

## See also {#section-d232fff7237443cc95c4bb50cb3d32bb}

[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) , [gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
