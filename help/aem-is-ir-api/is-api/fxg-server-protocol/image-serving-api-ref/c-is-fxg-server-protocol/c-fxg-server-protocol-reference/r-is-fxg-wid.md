---
description: View width. Specifies the width of the reply image (view image).
solution: Experience Manager
title: wid
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5edd045c-600e-4295-9672-04a5c3bc651d
---
# wid{#wid}

View width. Specifies the width of the reply image (view image).

 `wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Image width in pixels (int greater than 0), </p></td> 
 </tr> 
</table>

## Default {#section-830bae0b6bac440098444d7cdcb23e2e}

If neither `wid=`, `hei=`, nor `scale=` are specified, the reply image is the default view size specified in the FXG file.

Raster formats are rendered using the Default View Size (or the DefaultPix setting). Click **[!UICONTROL Application Setup]** > **[!UICONTROL Publish Setup]** > **[!UICONTROL Image Server]**, then enter your Width and Height values. Smaller sizes provide better performance. You must save your settings and perform an Image Serving Publish to apply a change.

If you apply a `scale=1` command, a raster format request is rendered at the size specified in the FXG.

## Example {#section-2f72cb2653d54c6aaacf0d97521fb72c}

[!DNL http://server/is/agm/myRootId/myImageId?wid=200]

Unless a format is specified, the image is rendered as a SWF file. In this case, height and width have no meaning, because the SWF usually expands to the size of the browser window. As a result, hei and wid only apply to raster or PDF formats. Raster formats include:

* GIF 
* TIF 
* PNG 
* JPG 
* JPEG 
* GIF-alpha 
* TIF-alpha 
* PNG-alpha
