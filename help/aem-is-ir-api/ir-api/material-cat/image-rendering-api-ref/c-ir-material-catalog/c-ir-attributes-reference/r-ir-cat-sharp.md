---
description: Default material sharpening. Sets the default material sharpening mode in case a particular catalog record does not contain a valid catalog Sharp value.


solution: Experience Manager
title: Sharp

feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# Sharp{#sharp}

Default material sharpening. Sets the default material sharpening mode in case a particular catalog record does not contain a valid catalog::Sharp value.

## Properties {#section-dcb810d01b8a40eb991d555a3cbe48b9}

Enum.

<table id="simpletable_2D94A380BC2D4FD1A7EDD45E6EAFD1FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>No sharpening. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Normal sharpening (after the transform). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Alternate sharpening (before the transform). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>More sharpening (both before and after the transform). </p> </td> 
 </tr> 
</table>

## Default {#section-613130fca7c04ce7a7734265f27aa1ea}

Inherited from `default::Sharp` if not defined or if empty.

## See also {#section-7771824f2822443ab0297e8793bb48ae}

[catalog::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) , [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a), [catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711) 
