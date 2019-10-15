---
description: You can create a set of thumbnail images from all or some of the images in a single folder.
seo-description: You can create a set of thumbnail images from all or some of the images in a single folder.
seo-title: Creating Thumbnails for a Set of Images
solution: Experience Manager
title: Creating Thumbnails for a Set of Images
topic: Scene7 Image Authoring
uuid: 6246b85f-076c-435e-8d5b-219d604db0e2
---

# Creating Thumbnails for a Set of Images{#creating-thumbnails-for-a-set-of-images}

You can create a set of thumbnail images from all or some of the images in a single folder.

When you save the thumbnails, you also create a file containing the RGB values for the dominant (base) color of each image and the width and height of the original image. After you specify these options, you can choose the folder containing the images whose thumbnails you want to generate.

**To create thumbnails:**

1. From the [!DNL Start] menu on your computer desktop, choose **[!UICONTROL Programs]** > **[!UICONTROL Scene7]** > **[!UICONTROL Image Authoring]** > **[!UICONTROL Content Authoring Tool.]**
1. In the [!DNL Content Authoring] tool, choose **[!UICONTROL File]** > **[!UICONTROL New]**.
1. In the **[!UICONTROL New]** dialog box, select [!DNL Thumbnail], then click **[!UICONTROL OK]**.
1. In the [!DNL Thumbnail Generation] dialog box, specify the following:

    * **Thumbnail Size**
    Specify the desired width and height for the thumbnails, in pixels. 
    * **Output File Type**
    Specify whether the generated thumbnails should be saved in bitmap, JPEG, PNG, TGA, or TIF format. 
    * **Generation options**
    Choose one of the following:

      * **Manual**
      Lets you define the area of the image to use in the thumbnail.

      * **Automatic Full Size**
      Crops and scales the image as needed to create a thumbnail of the size you specified.

      * **Automatic Full Size (Preserve Aspect Ratio)**
      Inserts blank space when cropping and scaling the image to the size you specified to maintain its aspect ratio.

      * **Automatic Fixed Size with a Size Ratio of**
      Crops and scales the image as needed to create the thumbnail after zooming in by the factor you specify. 
    
    * **Selected Files/All Sub-directories**
    Choose [!DNL Selected Files] to Ctrl-click the files whose thumbnails you want to generate. Choose [!DNL All sub-directories] to automatically generate thumbnails for all images in the directory you specify and all its sub-directories. 
    
    * **Output Data File**
    Specify a name for the file that contains the RGB and size information for these images. 
    * **Format for Input File Names**
    To process only a certain set of images, use the wildcard character &#42; (asterisk) to stand for the base filename and pre-pend a prefix and/or append a suffix. For example, [!DNL catalog_*.jpg] processes only images whose file names start with [!DNL catalog_] and end with [!DNL *.jpg] . 
    
    * **Format for Output File Names**
    Specify a prefix and suffix for the output file names, if desired. Specifying %s place the output thumbnails in the same sub-directory structure as the originals. 
    * **Input Image Size Threshold:**
    Specify the largest size for each image you process.

1. Click **[!UICONTROL OK]**.
1. In the [!DNL Select Image Directory] dialog box, specify the folder for the images to process.
If you chose [!DNL Selected] files, use the Shift key and Ctrl key to select the individual files to process, then click **[!UICONTROL OK]** in the dialog box. If you chose [!DNL All sub-directories], you cannot select individual files. 
