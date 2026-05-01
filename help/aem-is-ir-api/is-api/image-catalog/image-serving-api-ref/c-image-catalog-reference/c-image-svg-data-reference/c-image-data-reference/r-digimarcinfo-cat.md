---
title: DigimarcInfo
description: Digimarc image info. Enables Digimarc embedding and specifies the type of watermark and any associated image-specific data.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 87f4d8f0-02b9-4511-9151-89c58116c78d
TQID: https://experienceleague.adobe.com/evDSv9opxhAZscFMYDCRLsy8tYTveW1PrNwPExhgbeM
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
# DigimarcInfo{#digimarcinfo}

Digimarc image info. Enables Digimarc embedding and specifies the type of watermark and any associated image-specific data.

## Properties {#section-62af219e8bac422b8541841221c9ce4f}

Four integer values, separated by commas.

`*`type`*, *`flags`*, *`val1`*, *`val2`*`

`*`type`*` enables Digimarc embedding and specifies the watermark type: 

<table id="table_3648951F14D94C5BAD097CFB783F1EE7"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> type</span> </span> </p> </th> 
   <th class="entry"> <p><b>Watermark Type</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>None. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>Basic. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>Image ID. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>Transaction ID. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>Copyright years. </p> </td> 
  </tr> 
 </tbody> 
</table>

`*`flags`*` is a bit field with three values. Set bit 0 to indicate copy-protected content, bit 1 to indicate restricted content, and bit 2 to indicate adult content: 

<table id="table_00F218515FBE484F9D05CBAF14F9D045"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> flags</span> </span> </p> </th> 
   <th class="entry"> <p><b>Description</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>- </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>Copy-protected. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>Restricted. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>Copy-protected, restricted. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>Mature content. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>5</b> </p> </td> 
   <td> <p>Copy protected, adult content. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>6</b> </p> </td> 
   <td> <p>Restricted, adult content. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>7</b> </p> </td> 
   <td> <p>Copy-protected, restricted, mature content. </p> </td> 
  </tr> 
 </tbody> 
</table>

The interpretation of `*`val1`*` and `*`val2`*` depend on `*`type`*`: 

<table id="table_6B29F76BC1974C12AB7124BF84B29EC2"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> type</span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val1 </span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val2 </span> </span> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>Not used. </p> </td> 
   <td> <p>Not used. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>Not used. </p> </td> 
   <td> <p>Not used. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>Image ID. </p> </td> 
   <td> <p>Not used. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>Transaction ID. </p> </td> 
   <td> <p>Not used. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>First copyright year. </p> </td> 
   <td> <p>Second copyright year. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Default {#section-4bb97e5f79074be89cc691e73449eb43}

Inherited from attribute::DigimarcInfo if the field is not present or if it is empty.

## Examples {#section-0f14727a0a2a408781c9df71fed7f42d}

"0,0,0,0" disables Digimarc watermarking for this image.

"1,5,0,0" specifies a basic watermark with the adult and copy-protected content flag set.

"2,0,4567,0" specifies a watermark with an image ID.

"3,2,56483,0" specifies a watermark with a transaction ID and the restricted content flag set.

"4,0,1998,2001" specifies a watermark with copyright years.

## See also {#section-4bd3e7272c5c4b8cb8c5ca1ac7ed1012}

[attribute::DigimarcInfo](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcinfo.md#reference-de88636cb9b4435a94e3d0a80f072667) , [attribute::DigimarcId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcid.md#reference-33e3eca7f1874510904e5c8645cecd68)
