---
description: The following fields are recognized in image and SVG data files.
seo-description: The following fields are recognized in image and SVG data files.
seo-title: Image_SVG data
solution: Experience Manager
title: Image_SVG data
topic: Scene7 Image Serving - Image Rendering API
uuid: 6f9595b3-d448-4aa1-87fe-edddfdd48873
---

# Image_SVG data{#image-svg-data}

The following fields are recognized in image and SVG data files.

## Catalog management {#section-1056bcc3b6d04166b3aa6ec48913b6b2}

<table id="table_823F89CAD494441690D28F18005F774C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="r_id_cat.md#reference_C3F3CE9AAAC4451796A846D6722383E5" type="reference" format="dita" scope="local"> Id</a></span> </p> </td> 
   <td colname="col2"> <p>Catalog record identifier (index key). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Request attributes {#section-cfe69bcdcd4b4d129e99d11b9078ae4a}

<table id="table_C070C676835F49918E1B3BBF81471B09"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba" type="reference" format="dita" scope="local"> DigimarcInfo</a></span> </p> </td> 
   <td colname="col2"> <p>Image-specific info for Digimarc embedding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a" type="reference" format="dita" scope="local"> Expiration</a></span> </p> </td> 
   <td colname="col2"> <p>Cache expiration (time-to-live) for reply images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="r_modifier_cat.md#reference_D2C6884B3A2248FAB81A112D27969834" type="reference" format="dita" scope="local"> Modifier</a> </span> </p> </td> 
   <td colname="col2"> <p>Prefix request modifiers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="r_postmodifier_cat.md#reference_4BC3738A812B4E7C8A180E27BFBD770B" type="reference" format="dita" scope="local"> PostModifier</a> </span> </p> </td> 
   <td colname="col2"> <p>Postfix request modifiers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded" type="reference" format="dita" scope="local"> TimeStamp</a></span> </p> </td> 
   <td colname="col2"> <p>File modification time stamp. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Image attributes {#section-74c4d124255d4218ade87d7d1677c76d}

<table id="table_F2A33C2EB17A4EACB00DDEF7FB1BB0D4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="r_anchor_cat.md#reference_3AE039791E6644549399E8AEB503DDCF" type="reference" format="dita" scope="local"> Anchor</a></span> </p> </td> 
   <td colname="col2"> <p>Image anchor point. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="r_maskpath_cat.md#reference_F82B42535FFF42959E74A7C1E605C931" type="reference" format="dita" scope="local"> MaskPath</a></span> </p> </td> 
   <td colname="col2"> <p>Mask file path. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="r_path_cat.md#reference_306AFCAFF172440CA81B85DA8D78213C" type="reference" format="dita" scope="local"> Path</a></span> </p> </td> 
   <td colname="col2"> <p>Image/SVG file path. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5" type="reference" format="dita" scope="local"> PrintResolution</a></span> </p> </td> 
   <td colname="col2"> <p>Print resolution. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1" type="reference" format="dita" scope="local"> Resolution</a></span> </p> </td> 
   <td colname="col2"> <p>Object resolution. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="r_size_cat.md#reference_5A82CFE33ABE445998C586FFB6820A47" type="reference" format="dita" scope="local"> Size</a></span> </p> </td> 
   <td colname="col2"> <p>Image size. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Thumbnail attributes {#section-c5ac27bcd4224a80b7f42ead249027b1}

<table id="table_E07909B6C16F4D9686ADA381A4178E25"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69" type="reference" format="dita" scope="local"> ThumbRes</a></span> </p> </td> 
   <td colname="col2"> <p>Thumbnail resolution. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03" type="reference" format="dita" scope="local"> ThumbType</a></span> </p> </td> 
   <td colname="col2"> <p>Thumbnail type. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Auxiliary data {#section-bff4e1f9af9d45f1872abac3b414a629}

<table id="table_B6A9A702F533494E85CEC1AD42EC728A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="r_assettype_cat.md#reference_6177CCBCBA05496E9017D53FD898BCA3" type="reference" format="dita" scope="local"> AssetType</a></span> </p> </td> 
   <td colname="col2"> <p>Asset type. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="r_imageset_cat.md#reference_4764D347AFD64AFDAEDE9A74C7565256" type="reference" format="dita" scope="local"> ImageSet</a></span> </p> </td> 
   <td colname="col2"> <p>Image set data. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="r-map-cat.md" type="reference" format="dita" scope="local"> Map</a></span> </p> </td> 
   <td colname="col2"> <p>Image map data. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="r_targets_cat.md#reference_4C3865D34A34421786F2A4070955575A" type="reference" format="dita" scope="local"> Targets</a></span> </p> </td> 
   <td colname="col2"> <p>Zoom target data. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="r_userdata_cat.md#reference_1E552AEAD08E41489E82EC16936BC0DF" type="reference" format="dita" scope="local"> UserData</a></span> </p> </td> 
   <td colname="col2"> <p>User-defined data. </p> </td> 
  </tr> 
 </tbody> 
</table>

