---
description: Settings that help improve image sharpness for optimized pyramid TIF files.


solution: Experience Manager
title: UnsharpMaskOptions

feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
---

# UnsharpMaskOptions{#unsharpmaskoptions}

Settings that help improve image sharpness for optimized pyramid TIF files.

 `unsharpMaskOptions=[ *`amount, radius, threshold, monochrome`*]` 

## Parameters {#section-c3f0d03136ba4422819cb463bd393885}

Specify a value for `unsharpMaskOptions` options with `minOccurs=" *`n`*".`

<table id="table_D1392963C5694969A9D546F82DB6F45C">
 <thead>
  <tr>
   <th colname="col1" class="entry"> Name </th>
   <th colname="col2" class="entry"> Type </th>
   <th colname="col3" class="entry"> Description </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> amount</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:double</span></td>
   <td colname="col3"><p>Controls contrast applied to edge pixels. 
     <ul id="ul_7AA17E354EE64BC4A5BEAE853FF17191">
      <li id="li_42FB21C7ED884E1DB03274130B8DCB10">Range: 0.0 - 5.0 </li>
      <li id="li_E980CAA1A9C54D60A121F21C964820FF">Default: 0 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> radius</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:double</span></td>
   <td colname="col3"><p>Controls sharpness by setting the number of pixels around the edge of an image. The correct value depends on the size of the image. 
     <ul id="ul_D4391CD407DE4B48AF4523EBD85D0D40">
      <li id="li_8AEF11A489484EFD91416F8A03C4DB25">Range: 0.0 - 250.0 </li>
      <li id="li_9F1D1B52AFBA46B8BDCDF99A21140002">Low values sharpen edge pixels only. </li>
      <li id="li_7D9FD8AA4899404283D7AB596364A4AF">High values sharpen a wider band of pixels. </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> threshold</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:int</span></td>
   <td colname="col3"><p>Determines how different pixels must be from the surrounding area before they are considered edge pixels and can be sharpened. 
     <ul id="ul_117E556E3ECF42CC878DD80D338D19CA">
      <li id="li_CFEE76DB78BF437E8463C9089486F8A6">Range: 0 - 255 (integers only). </li>
      <li id="li_77113DC2698A4D48B11288718766E6A2">Default: 6 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> monochrome</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:int</span></td>
   <td colname="col3"><p>Values include <span class="codeph"> 0</span> or <span class="codeph"> 1</span> only. </p><p>Set to <span class="codeph"> 0</span> to apply to each color component separately or to <span class="codeph"> 1</span> to apply to image brightness (intensity) only. The layer mask or composite mask is sharpened as well . </p><p><span class="codeph"><span class="varname"> monochrome</span></span> is ignored for grayscale images. </p></td>
  </tr>
 </tbody>
</table>

## Example {#section-38adca96c7714cfea35331d20403f59e}

```
<element name="unsharpMaskOptions" type="types:UnsharpMaskOptions" minOccurs="0"/>
    <complexType name="UnsharpMaskOptions">
        <sequence>
            <element name="amount" type="xsd:double" minOccurs="0"/>
            <element name="radius" type="xsd:double" minOccurs="0"/>
            <element name="threshold" type="xsd:int" minOccurs="0"/>
            <element name="monochrome" type="xsd:int" minOccurs="0"/>        
        </sequence>
    </complexType>
```

## Used by {#section-db8124a5468b498694a780f8a56a4560}

The `unsharpMaskOptions` type is used by:

* [ReprocessAssetsJob](../../types/c-data-types/r-reprocess-assets-job.md#reference-a303f7832ae44fdab1dca7cc8bef3fa3)
* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

>[!MORELIKETHIS]
>
>* [Image Serving API Reference: op_usm](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-serving-api/image-serving-api/http-protocol-reference/command-reference/r-op-usm.html)
