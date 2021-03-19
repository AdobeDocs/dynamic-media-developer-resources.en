---
description: View height. Specifies the height of the reply image.
seo-description: View height. Specifies the height of the reply image.
seo-title: hei
solution: Experience Manager
title: hei
uuid: 6f7e580b-6399-4661-b5d9-8044574ba124
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Business Practitioner"
---

# hei{#hei}

View height. Specifies the height of the reply image.

 `hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Image height in pixels (int greater than 0). </p></td> 
 </tr> 
</table>

Raster formats are rendered using the Default View Size (or the DefaultPix setting). Click **[!UICONTROL Application Setup]** > **[!UICONTROL Publish Setup]** > **[!UICONTROL Image Server]**, then enter your Width and Height values. Smaller sizes provide better performance. You must save your settings and perform an Image Serving Publish to apply a change.

If you apply a `scale=1` command, a raster format request is rendered at the size specified in the FXG.

## Default {#section-76ee3daa77cb468ab310821357cc9404}

If neither `wid=`, `hei=`, nor `scale=` are specified, the reply image is the default view size specified in the FXG file.

## Example {#section-a91c14d31e71481ba054412d9f642885}

[!DNL http://server/is/agm/myRootId/myImageId?hei=200]

Unless a format is specified, the image is rendered as a SWF file. In this case, height and width have no meaning, because the SWF usually expands to the size of the browser window. As a result, hei and wid only apply to raster or PDF formats. Raster formats include:

* GIF 
* TIF 
* PNG 
* JPG 
* JPEG 
* GIF-alpha 
* TIF-alpha 
* PNG-alpha

