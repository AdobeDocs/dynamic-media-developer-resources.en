---
description: Gloss map image. Provides pixel-by-pixel control of the glossiness of a repeatable texture, wallpaper/border, or decal.
solution: Experience Manager
title: glossmap
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 922fc527-be19-4d7a-b265-7bdb1de80990
---
# glossmap{#glossmap}

Gloss map image. Provides pixel-by-pixel control of the glossiness of a repeatable texture, wallpaper/border, or decal.

 `glossmap={ *`glossMapFile`*| *`embeddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> embeddedReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&lbrace;'is&lbrace;'<span class="varname"> isReq</span>'&rbrace;'&rbrace;|&lbrace;'&lbrace;'<span class="varname"> foreignReq</span>'&rbrace;' </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> glossMapFile</span> </span> </p></td> 
  <td class="stentry"> <p>Gloss map image file (grayscale). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> isReq</span> </span> </p></td> 
  <td class="stentry"> <p>Request to Image Server. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> foreignReq </span> </span> </p></td> 
  <td class="stentry"> <p>Request to a foreign server. </p></td> 
 </tr> 
</table>

Applicable for materials such as metallic paint effects, die-cut foil wallpapers and borders, metallic thread fabrics, and so forth.

The gloss map image must be 8-bit grayscale and have exactly the same size as the primary image specified with `src=`. Refer to the description of [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) for additional information.

## Properties {#section-26375672d69849be9b026cc93c3bc558}

Material attribute. Supported by repeatable textures, wallpapers and borders, and decals. Ignored by solid color, cabinet, and window covering materials. See [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) for additional information.

## Default {#section-d9ac031fb2f94482ac3fe2283d7cb168}

None.

## See also {#section-33953fc1be82452da37141f2e541e00c}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca), [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
