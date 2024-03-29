---
title: op_noise
description: Add noise. Adds random noise to the foreground image data, or to the foreground of an effect layer.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eeadd3ab-80ff-4f9b-b5b7-4f3da6feebde
---
# op_noise{#op-noise}

Add noise. Adds random noise to the foreground image data, or to the foreground of an effect layer.

 `op_noise= *`val`*[,uniform|gaussian[, *`monochrome`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> val</span> </p> </td> 
   <td colname="col2"> <p>Amount of noise in percent (0…100 int). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> uniform</span> </p> </td> 
   <td colname="col2"> <p>Select uniform noise distribution. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> gaussian</span> </p> </td> 
   <td colname="col2"> <p>Select gaussian noise distribution. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> monochrome</span> </p> </td> 
   <td colname="col2"> <p>Set to 0 for color noise, 1 for gray noise. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`monochrome`* is ignored for grayscale images.

## Properties {#section-1f1a64c791f545a3bf1abd0b0e575d87}

Layer command. Applies to the current layer or to the composite image if `layer=comp`.

## Default {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`, for no noise.
