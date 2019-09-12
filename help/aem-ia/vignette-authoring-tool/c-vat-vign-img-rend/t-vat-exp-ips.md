---
description: If you use the Image Production System, you can export vignettes and images directly to IPS.
seo-description: If you use the Image Production System, you can export vignettes and images directly to IPS.
seo-title: Exporting to IPS
solution: Experience Manager
title: Exporting to IPS
topic: Scene7 Image Authoring
uuid: 9f8f3fdb-85d0-464d-a25c-4ce979e8acf1
index: y
internal: n
snippet: y
---

# Exporting to IPS{#exporting-to-ips}

If you use the Image Production System, you can export vignettes and images directly to IPS.

 Make sure you have [configured IPS preferences](../c-vat-img-auth-opt/t-vat-config-ips-settings.md#task-a58a6c7d64a3442c9c7e4f62ef99f9a8) first. You can also [batch-render the objects in your vignette and export the resulting rendered images directly to IPS](../c-vat-rend-pg/c-vat-rend-obj/t-vat-batch-rend-ips.md#task-f89e8d1a7bc54694b14173505641a0df).

**To Export an Image to IPS:** 

1. On the [!DNL File] menu, click **[!UICONTROL Export to IPS]**.
1. In the [!DNL IPS Export] dialog box, specify the following:

    * **Object Name:** In the drop-down list at the right side of the field, choose the file type you are exporting. You can choose to export a vignette or a rendered vignette in the form of an image file.

      IPS converts all images to pyramid TIF for efficient storage and easy conversion to other formats. You can also specify the default format for these images when they are deployed. BMP and TIF files take longer to upload.

      In the field, specify the base name for the item in the IPS. 
    
    * **Company:** Specify the company in the IPS under which these images appear. The list contains only the companies to which you have access in IPS. 
    * **Folder:** Indicate the target folder in IPS where you want these items to be stored.

      For images, you can select the folder from the hierarchy list, if folders already exist in IPS for the specified company, and you [checked [!DNL Browse IPS Folders] in the [!DNL IPS Preferences] dialog box](../c-vat-img-auth-opt/t-vat-config-ips-settings.md#task-a58a6c7d64a3442c9c7e4f62ef99f9a8). The path to this folder appears in the field below the list.

      To add a folder, select its parent and add [!DNL \Foldername] at the end of its name, where "Foldername" is the name of the folder to add. For example, to add a folder called "MyVignettes" under an existing folder called "Vignettes," you would click in the "Vignettes" folder name and type "\MyVignettes" at the end of its name. If your server uses Linux, folder and filenames are case-sensitive.

      If the folder hierarchy in IPS is very extensive, the list of folders may take a while to load. 
    
    * **Project(s):** Indicate any IPS project to which you want these images to belong.

1. If the items you are exporting are ready to publish, check the [!DNL Ready to Publish] checkbox.
1. Click **[!UICONTROL OK]**.

   Use the [!DNL My Logs] feature in IPS to check the success or failure of uploads to IPS. 

