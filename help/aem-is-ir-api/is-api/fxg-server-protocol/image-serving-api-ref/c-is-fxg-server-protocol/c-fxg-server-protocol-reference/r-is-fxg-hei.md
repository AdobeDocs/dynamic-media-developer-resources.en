---
title: hei
description: View height. Specifies the height of the reply image.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dcc9311d-4157-490b-9fc4-47060ddb0e37
TQID: 'https://experienceleague.adobe.com/Tpl8zVXQVzs3isa26A3YvnOzs6gqpz3-4L-qDBx-eK0'
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
# hei{#hei}

View height. Specifies the height of the reply image.

 `hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Image height in pixels (int greater than 0). </p></td> 
 </tr> 
</table>

Raster formats are rendered using the Default View Size (or the DefaultPix setting). Select **[!UICONTROL Application Setup]** > **[!UICONTROL Publish Setup]** > **[!UICONTROL Image Server]**, then enter your Width and Height values. Smaller sizes provide better performance. Save your settings and perform an Image Serving Publish to apply a change.

If you apply a `scale=1` command, a raster format request is rendered at the size specified in the FXG.

## Default {#section-76ee3daa77cb468ab310821357cc9404}

If `wid=`, `hei=`, or `scale=` are not specified, the reply image is the default view size specified in the FXG file.

## Example {#section-a91c14d31e71481ba054412d9f642885}

[!DNL `http://server/is/agm/myRootId/myImageId?hei=200`]

Unless a format is specified, the image is rendered as a SWF file. In this case, height and width have no meaning, because the SWF usually expands to the size of the browser window. As a result, hei and wid only apply to raster or PDF formats. Raster formats include:

* GIF 
* TIF 
* PNG 
* JPG 
* JPEG 
* GIF-alpha 
* TIF-alpha 
* PNG-alpha
