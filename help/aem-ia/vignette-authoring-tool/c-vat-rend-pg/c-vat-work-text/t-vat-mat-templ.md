---
description: Material templates are sets of properties that you can apply to a material.
seo-description: Material templates are sets of properties that you can apply to a material.
seo-title: Using Material Templates
solution: Experience Manager
title: Using Material Templates
topic: Scene7 Image Authoring
uuid: 078bcfe2-2351-4af1-a70b-62d3ff1ac55a
index: y
internal: n
snippet: y
---

# Using Material Templates{#using-material-templates}

Material templates are sets of properties that you can apply to a material.

You can create a material template for a texture, color, or window covering, but if the template contains settings that are not appropriate for a material when you apply it, those settings are ignored. For example, sharpening settings are ignored for colors.

If you apply a template to a material in a vignette, its settings become the active settings for that material, so that anyone else opening the vignette with that material sees the same settings. The templates themselves are needed only when you set up a material.

You can save material templates on your local system in [!DNL .VTC] (Vignette Template Collection) files to share with other [!DNL Image Authoring] users.

There is one special material template called VIGNETTE. This template is saved with the vignette itself and is used as the default settings for all materials, if no other template or settings are specified. The VIGNETTE template is not saved out to a file.

**To Create a Material Vignette:** 

1. On the [!DNL Render] page, apply a texture or color to a masked object.
1. Right-click the applied texture and choose **[!UICONTROL Properties]**.
1. In the [!DNL Texture Material Properties] dialog box, click the **[!UICONTROL General]** tab and choose **[!UICONTROL Manage Templates]** from the [!DNL Template] drop-down list.

   You can also change settings on the [!DNL Texture Material Properties] dialog box, then choose **[!UICONTROL Manage Templates]**. Your new settings are the starting values on the [!DNL Material Templates] dialog box.
1. In the [!DNL Material Templates] dialog box, specify a name for the new template, or choose an existing template from the list on the left.

   If you choose an existing template, you modify the settings for that template.

   You cannot choose the VIGNETTE template until you save settings to it. 

1. Specify settings on each tab of the dialog box. The settings are the same as those on the [ [!DNL Texture Material Properties]](../../c-vat-rend-pg/c-vat-work-text/c-vat-text-mat-prop/c-vat-text-mat-prop.md#concept-56e919cfd48748169dc2f011aa95c5fd) dialog box.
1. Do any of the following:

    * To create a new template, click **[!UICONTROL New]**. (This button is available only if you typed a unique name for this template.) 
    * To modify the existing template you selected, click **[!UICONTROL Save]**. 
    * To return the settings to their previous values, click **[!UICONTROL Reset]**. 
    * To delete a template from the list on the left, select the template, click **[!UICONTROL Action]**, then choose the **[!UICONTROL Delete]** option. 
    
    * To save the current settings as the default for all future materials in this vignette, click **[!UICONTROL Action]**, then choose **[!UICONTROL Copy to 'VIGNETTE']** template. This causes the VIGNETTE item in the list on the left to become active. 
    
    * To save your material templates to a file, click **[!UICONTROL Action]**, and choose **[!UICONTROL Save Templates to File]**. 
    
    * To import material templates from a file, click **[!UICONTROL Action]**, then choose **[!UICONTROL Load Templates from File]**.

      You can also right-click a template in the list on the left to see the choices that appear on the [!DNL Action] button.

1. To apply the selected template in the list on the left to the current material on the [!DNL Render] page, click **[!UICONTROL OK]**. To close the dialog box without applying the template, click **[!UICONTROL Close]**.
