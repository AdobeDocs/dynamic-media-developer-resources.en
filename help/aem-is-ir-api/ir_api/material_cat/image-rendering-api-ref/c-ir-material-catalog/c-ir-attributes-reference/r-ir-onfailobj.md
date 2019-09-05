---
description: Object selection error handling. Specifies the action to be taken if the obj= command fails because the specified path cannot be matched in the vignette object hierarchy.
seo-description: Object selection error handling. Specifies the action to be taken if the obj= command fails because the specified path cannot be matched in the vignette object hierarchy.
seo-title: OnFailObj
solution: Experience Manager
title: OnFailObj
topic: Scene7 Image Serving - Image Rendering API
uuid: 5dd29e42-81d0-4c35-a9db-3cd8279eb595
index: y
internal: n
snippet: y
---

# OnFailObj{#onfailobj}

Object selection error handling. Specifies the action to be taken if the obj= command fails because the specified path cannot be matched in the vignette object hierarchy.

## Properties {#section-2c779d9c133a443d9f0aed9fde7b703c}

Enum.

<table id="simpletable_538B76AB784D4DEE9B8021A6BDCE06AB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Inherit from <span class="codeph"> default::OnFailObj </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Keep the previous selection. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>Deselect; any attempts to apply a material or show/hide objects will be ignored. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Return an error. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Select the default group (the first group in the vignette hierarchy that contains renderable objects). </p> </td> 
 </tr> 
</table>

## Default {#section-a5a95a2b4a204a4eae350e5b544d1513}

Inherited from `default::OnFailObj` if not defined.

## See also {#section-806dc2c5973c41f683af085b3315043c}

[obj=](../../../../../ir_api/http_protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) , [attribute::OnFailSel](../../../../../ir_api/material_cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513) 
