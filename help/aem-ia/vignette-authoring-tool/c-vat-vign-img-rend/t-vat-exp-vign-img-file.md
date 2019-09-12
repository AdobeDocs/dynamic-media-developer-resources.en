---
description: You can export (save) a vignette as one of several graphic file types, including PNG, JPEG, Photoshop (PSD), TIFF, and bitmap.
seo-description: You can export (save) a vignette as one of several graphic file types, including PNG, JPEG, Photoshop (PSD), TIFF, and bitmap.
seo-title: Exporting a Vignette to an Image File
solution: Experience Manager
title: Exporting a Vignette to an Image File
topic: Scene7 Image Authoring
uuid: f5d34e4c-fffa-4225-9542-f0e4aef540bd
index: y
internal: n
snippet: y
---

# Exporting a Vignette to an Image File{#exporting-a-vignette-to-an-image-file}

You can export (save) a vignette as one of several graphic file types, including PNG, JPEG, Photoshop (PSD), TIFF, and bitmap.

For [!DNL Photoshop] (PSD), PNG, TIFF, and JPEG files, you can specify a default print resolution (in dots per inch), as well as color conversion options. For JPEG files, you can also change the amount of compression used when the image is saved, which affects the image quality. For TIFF files, you can indicate whether to use LZW compression when the image is saved. For PSD files, you can choose compression to be none or RLE. Images exported to PSD using [!DNL Export to Image File] are flat images.

**To Save a Vignette in a Graphic File Format:** 

1. On the [!DNL File]menu, click **[!UICONTROL Export]**.
1. In the [!DNL Export to Image File] dialog box, navigate to the folder you want.
1. Enter a name in the [!DNL File] name box.
1. Click the **[!UICONTROL Save as type]** box, then choose the file type you want.

       Depending on the file type you choose, [!DNL Image Authoring] may prompt you for further choices:

       **PNG, TIFF, PSD, and JPEG:** If you choose PSD, PNG, TIFF, or JPEG as the export format, specify a default print resolution (in dots per inch). (PNG is a metric format, so the dots-per-inch value is converted.)

       When you export to PSD, TIFF, or PNG on the [!DNL Render Page], you can include an alpha channel. To do this, set [!DNL Alpha Usage] to None, All objects, or Selected object.

       If you have defined a working color space for this vignette, you can also specify whether to use the working color space or a different color space. (If you haven't defined a working color space, these options don't appear.)

    * If you keep the current working color space, the RGB values for your system are used to generate the new image. 
    * If you convert to a different color space, the RGB values are different from the ones you see on your screen, they are based on the new color space. Because computer monitors vary, different color spaces may depict colors more accurately on one monitor than on another. 
    * If you choose a different color space, specify a [!DNL Conversion Intent]. Choose from the standard ICC options that are listed. The conversion intent tells the color space conversion how to handle colors that are out of bounds for the new color space. 
    * In either case, specify whether to embed the color profile in the image or not. An embedded color profile lets an image-editing program interpret the RGB values correctly.

       **JPEG:** If you choose JPEG as the export format, you can also change the quality and encoding settings.

       The higher the [!DNL Quality] number, the less compression is used when saving the image. The less compression, the better the quality.

       The [!DNL Progressive] setting affects how images appear on a slow Internet connection. Standard encoding displays the image in full detail, but it displays a row of pixels at a time, starting from the top and progressing to the bottom. Progressive encoding displays the entire image at the same time, starting with a vague representation and filling in the detail as it displays.

       **TIFF:** This format lets you change image sizes later without degrading the image. If you choose TIFF as the export format, specify LZW compression or no compression. 
    
1. Click **[!UICONTROL Save]**.
You can save a vignette as a layered PSD ( [!DNL Photoshop]) file by batch-rendering the images, or you can [export to PSD format](../c-vat-gs/c-vat-work-ps/t-vat-exp-ps.md#task-acd68e2f66264c6ca8309905e43136d9). 
