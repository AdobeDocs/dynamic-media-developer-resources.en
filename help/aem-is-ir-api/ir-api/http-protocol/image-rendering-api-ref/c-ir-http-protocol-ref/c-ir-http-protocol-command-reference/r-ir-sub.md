---
title: sub
description: Sub selection. Permits applying different materials to different areas of the selected object or group, and removing previously applied materials.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c9968fbb-c38b-4180-81be-19992fa8f347
---
# sub{#sub}

Sub selection. Permits applying different materials to different areas of the selected object or group, and removing previously applied materials.

 `sub=0|1|2|3|4|5`

<table id="simpletable_F6BF91BD2C4B47BF8A28032E392D37F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Select the entire wall. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Select the upper half of the wall. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>Select the lower half of the wall. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Select the top wall border area. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Select the middle wall border area. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>Select the bottom wall border area. </p> </td> 
 </tr> 
</table>

Currently supported only for wall objects. Terminates a preceding MSS and starts a new MSS for the material to be applied to the specified subselection.

A material specified for either the upper or lower wall applies to the entire wall unless a different material for the other half of the wall has been specified as well.

## Properties {#section-b202139d6d0847cc8d520a154104ab9d}

Selection command; MSS delimiter.

## Default {#section-5b45a167a17c451596e4c59b7d53c368}

`sub=0`

## See also {#section-1a993ee24f144d4fb8baef0cc431b53b}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)
