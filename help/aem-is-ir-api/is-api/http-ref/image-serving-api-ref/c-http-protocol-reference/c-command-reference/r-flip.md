---
title: flip
description: Flip Layer. Flips the layer horizontally, vertically, or both, after applying crop= and before rotate= and extend=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 451d8b4d-0f22-41f3-ac86-435797c23ea3
TQID: 'https://experienceleague.adobe.com/7RG0rzG40Mp5eQe663S5Ayyf99SIfSLPHgqbSL2Unn4'
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
# flip{#flip}

Flip Layer. Flips the layer horizontally, vertically, or both, after applying crop= and before rotate= and extend=.

 `flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr </span> </p> </td> 
  <td class="stentry"> <p>Flip the layer horizontally (left-right). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud </span> </p> </td> 
  <td class="stentry"> <p>Flip the layer vertically (up-down). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lrud </span> </p> </td> 
  <td class="stentry"> <p>Flip both horizontally and vertically. </p> </td> 
 </tr> 
</table>

It may also be applied to text layers.

Some commands, including `extend=`, implicitly apply to layer 0 instead of the composite layer when `layer=comp` is selected. In such scenarios, all commands that are assigned automatically to layer 0 is applied before the commands which apply to `layer=comp`. Thus, when `layer=comp`, `extend=` is applied before `flip=`.

>[!NOTE]
>
>The flipped layer is positioned based on the layer anchor. Different `flip=` values result in different layer positions when the anchor is not at the center of the layer.

## Properties {#section-294da2af7be746b5adfc35e29ee68217}

Layer command. Applies to the current layer or to the composite image if `layer=comp`. Ignored by effect layers.

## Default {#section-502044f81a89492198d5f12a738459ea}

None.

## See also {#section-47f6484deccd420983df15ec163b4a83}

[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) , [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
