---
title: effect
description: Select Effect Layer. Selects an effect layer and starts a new layer segment in the request string, which is associated with the current layer.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1eaa38d-cfd3-44d4-92b1-04d72333f867
---
# effect{#effect}

Select Effect Layer. Selects an effect layer and starts a new layer segment in the request string, which is associated with the current layer.

 `effect= *`n`*`

<table id="simpletable_C48DABF486604D2B9F3CBC1CD01AC76D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p> </td> 
  <td class="stentry"> <p>Effect layer number (int not equal to 0). </p></td> 
 </tr> 
</table>

All commands within the new segment are applied to the specified effect layer. An effect layer segment is terminated by the next `layer=` or `effect=` command or by the end of the request.

The value *`n`* must be less than 0 for outer layer effects (that is, effects behind the parent layer) and greater than 0 for inner layer effects (that is, effects within the parent layer). Effect layer numbers do not have to be consecutive.

The effect layer number specifies the z-order, if there are multiple effect layers for the same parent layer. Higher-numbered layers are placed on top of lower-numbered layers.

Effect layers may be attached to `layer=comp`.

## Properties {#section-e11f795deff345779ce280a82cf221ca}

Effect layer command. The value *`n`* must not be 0.

## Default {#section-84bbe1cfe7a94040827c994323ac59d4}

None.

## Example {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## See also {#section-573273e9e0e64103a5764075f5e50180}

[layer=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md)
