---
description: Lets you crop to the bounding box of an embedded named path. This cropping, in turn, changes the size of the image.
seo-description: Lets you crop to the bounding box of an embedded named path. This cropping, in turn, changes the size of the image.
seo-title: cropPathE
solution: Experience Manager
title: cropPathE
uuid: 4689fd20-dfa0-47eb-8184-cd233f1ac088
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# cropPathE{#croppathe}

Lets you crop to the bounding box of an embedded named path. This cropping, in turn, changes the size of the image.

 `cropPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="table_598304852E844456AB3AC9FF1F178B71"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pathName</span></span> </p> </td> 
   <td colname="col2"> <p>Name of path embedded in layer source image (ASCII only). </p> <p> <span class="codeph"><span class="varname"> pathName</span></span> is the name of a path embedded in the layer source image. The path is automatically transformed as needed to maintain relative alignment with the image contents. If more than one <span class="codeph"><span class="varname"> pathName</span></span> is specified, the server crops to the bounding box of each path, one at a time. Any <span class="codeph"><span class="varname"> pathName</span></span> not found in the source image is ignored. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Layer attribute. Applies to the current layer or to the composite image if `layer=comp`. Ignored by effect layers.

`cropPathE=` is ignored if no path with the specified name is found in the layer source image, or if the layer source is not an image.

## Default {#section-d1986aa31af14767aeb1b4a57add67f4}

None, for no additional cropping of the layer.

## See also {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[crop](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab), [clipPathE](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) 
