---
description: You can configure settings for IPS (Image Production System) to support uploading images, materials, render sets, and layered files to IPS, and batch-rendering objects in your vignette and exporting the results directly to IPS.
seo-description: You can configure settings for IPS (Image Production System) to support uploading images, materials, render sets, and layered files to IPS, and batch-rendering objects in your vignette and exporting the results directly to IPS.
seo-title: Configuring IPS Settings
solution: Experience Manager
title: Configuring IPS Settings
topic: Scene7 Image Authoring
uuid: 9b0622fb-9533-4648-8413-68c1c57efbc6
---

# Configuring IPS Settings{#configuring-ips-settings}

You can configure settings for IPS (Image Production System) to support uploading images, materials, render sets, and layered files to IPS, and batch-rendering objects in your vignette and exporting the results directly to IPS.

 **To Configure IPS Settings:** 

1. From the [!DNL Edit] menu, choose **[!UICONTROL Preferences]** and click the **[!UICONTROL IPS]** tab.
1. Fill in the fields on the [!DNL IPS] tab as follows:

    * **Server Name/Address:** Specify the name of your IPS server, for example, s7northips. 
    * **Website Root Directory:** If IPS is installed in a subdirectory, type that location name here. 
    * **E-mail (IPS User ID):** Specify the email address you use to log into IPS. 
    * **Password (IPS):** Specify the password you use when you log into IPS with the email address you specified above. 
    * **IPS Vignette Download Directory:** Indicate where you want vignettes to reside when you drag and drop them from IPS. 
    * **Texture Width/Height Limit:** IPS images may be hundreds of megabytes in size. If you try to add an image to [!DNL Image Authoring] from the IPS and the image is larger than the size limit set here, [!DNL Image Authoring] tries to scale the image down to a size within these limits. This helps reduce download time and cache size requirements. [!DNL Image Authoring] leverages the Microsoft Internet Explorer browser cache-set your browser cache to a suitable value. 
    
    * ** IS Request Modifiers:** You can specify parameters to apply to textures you [drag and drop](../c-vat-rend-pg/c-vat-rend-obj/t-vat-drag-text.md#task-cad3f740e6194876b25ca2704630aeec) between the [!DNL Image Production System] and [!DNL Image Authoring]. Specify these parameters as you would in an IPS URL. You can safely specify the parameters that follow:

      File Format: [!DNL fmt=jpeg], png, png-alpha, tif, or tif-alpha

      JPEG quality (if you specified jpeg as the file format): [!DNL qlt=1-100]

      Sharpening: [!DNL op_sharpen=1] (to sharpen the image)

      Caching (to disable caching of the image on the client and server): [!DNL cache=off]

      ICC color profile embedding: [!DNL iccEmbed=1]

      If the default RGB ICC color profile is set in IPS and you set iccEmbed, the color profile is embedded in the dropped image. If the default in IPS is not set, this setting is ignored. A Company Administrator or an IPS administrator must set the RGB ICC color profile default and upload the ICC color profiles. For information about setting and publishing color profiles, see the IPS Help.

      Also, in order to embed the color profile, the color space needs to be appended to the [!DNL fmt=] modifier. For example, the adjustment would look something like this: [!DNL fmt=tif,rgb]

      Do not specify any parameters that would change the size of the returned image (such as wid=, hei=, scl=, res=, size=, crop=, extend=, req=tmb, etc), because that can cause problems with image resolution. 
    
    * **Browse IPS Folders:** Check this option to be able to view the folder hierarchy in the [ [!DNL IPS Export] dialog box](../c-vat-vign-img-rend/t-vat-exp-ips.md#task-a3367d2830a544e99bca84633b7fee7d). Uncheck this option to make the folder hierarchy not display. You must know the path and type it manually. If IPS is on a Linux server, the folder names are case-sensitive. 
    
    * **Background Batch Upload:** Check this option to be able to continue using [!DNL Image Authoring] while performing a [batch render or render set upload to IPS](../c-vat-rend-pg/c-vat-rend-obj/t-vat-batch-rend-ips.md#task-f89e8d1a7bc54694b14173505641a0df). [!DNL Image Authoring] informs you when it is done uploading.

1. Click **[!UICONTROL OK]**.
