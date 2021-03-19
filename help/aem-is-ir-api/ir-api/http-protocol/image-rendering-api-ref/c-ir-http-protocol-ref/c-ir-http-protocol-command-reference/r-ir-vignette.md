---
description: Vignette file. Specifies the vignette to be used for this request.
seo-description: Vignette file. Specifies the vignette to be used for this request.
seo-title: vignette
solution: Experience Manager
title: vignette
uuid: 8bba4ad4-bd55-4c55-8ebf-585371cf33f1
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# vignette{#vignette}

Vignette file. Specifies the vignette to be used for this request.

 `vignette=[ *`catId`*/] *`recId`*|[catId/] *`file`*`

<table id="simpletable_432EC5501CA3431B83A762C3EE4E8DD2"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p> </td> 
  <td class="stentry"> <p>Material catalog id (matched to <span class="codeph"> attribute::RootId</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>Vignette ID (matched to <span class="codeph"> vignette::Id</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> file</span> </p></td> 
  <td class="stentry"> <p>Relative vignette file path and name. </p></td> 
 </tr> 
</table>

Can either specify a vignette map entry or a vignette file. Remote URLs are not permitted.

`vignette=` can be used as an alternative to specifying the vignette in the request URL path. Mainly used to specify vignettes via variables in templates.

If *`catId`* is not specified, the session catalog is used.

## Properties {#section-f58661fc78d7496e8e3d0fb98b945c4b}

May occur anywhere within the request. Overrides the vignette specified with the request URL path.

## Default {#section-db0618d48bc84dc8abcc989550349ccc}

None.

## See also {#section-dc2668cc2cd54a74b08cff68a12d4edd}

[Material Catalogs](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2), [Custom Variables](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-custom-variables/c-ir-custom-variables.md#concept-8a1d9a50d09a4b7b97b8c83365971f96) 
