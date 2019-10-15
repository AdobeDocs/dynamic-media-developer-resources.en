---
description: If you created and imported geometry to create a 3D vignette, you can add 3D objects.
seo-description: If you created and imported geometry to create a 3D vignette, you can add 3D objects.
seo-title: Creating 3D Objects
solution: Experience Manager
title: Creating 3D Objects
topic: Scene7 Image Authoring
uuid: c0e9e514-22ea-4493-9d2e-d46a59b0595c
---

# Creating 3D Objects{#creating-d-objects}

If you created and imported geometry to create a 3D vignette, you can add 3D objects.

 **To Create a 3D Object:** 

1. In the [ [!DNL Object Explorer]](../../r-vat-glossary/c-vat-obj-explorer.md#concept-da56038ea82c40a1a10576f99f2f6836), right-click the name of the group that contains the object.
1. Select the object type for the new object. The 3D object types are:

    * **New Non-Texturable Object:** For objects that accept color, but no texture. Use this option if you use this vignette on your [!DNL Image Rendering] server but will not apply textures to it, as these object types render faster. [!DNL Non-Texturable Objects] do not render decals. 
    
    * **New Planar Object:** For flat surfaces, such as countertops and floors, that don't have their own object type. For walls, cabinets, or doors, use the object types dedicated to those items. [!DNL Planar] objects accept paint and generic textures. Use cabinets to get cabinet textures.

      Later on, you can assign [ [!DNL Planar] objects to planes](../../c-vat-obj-pg/c-vat-abt-obj-pg/t-vat-assign-obj.md#task-e8ad247824b24fb0b05e115df24c45b6) so each one moves and resizes with its plane. 
    
    * **New Flowline or Sketch Object:** For upholstered objects that use a patterned material. You can create flowlines for a [!DNL Flowline] object, and for non-renderable, 3D objects that sit on reflective planes in your image. For example, use this object type for a vase that sits on a flat table, or the legs of a chair that sits on a shiny floor.

      Later on, you can [assign 3D [!DNL Flowline] and [!DNL Sketch] objects to planes](../../c-vat-obj-pg/c-vat-abt-obj-pg/t-vat-assign-obj.md#task-e8ad247824b24fb0b05e115df24c45b6) and [specify where the object meets the plane](../../c-vat-obj-pg/c-vat-obj-pg-tools/c-vat-edit-mod-tool/t-vat-persp-2d-obj.md#task-92347286decc483aba4c4ff7d258054c), so the object appears three-dimensional when you render it, and reflections render accurately. 
    
    * **New Window Coverings Frame:** A frame that [receives window treatments](../../c-vat-rend-pg/c-vat-rend-obj/c-vat-window-cov/t-vat-use-window-cov.md#task-57ae1754b3c84c9eabc3f52bf702fe7a). You cannot convert another object to or from this type. 
    
    * **New Wall, Cabinet, Appliance, and Door Object:** For walls, cabinets, appliances or doors.

      If you attached a template to this vignette, your choices include the objects that were saved with that template. For example, when you right-click, the list might look like this:

      ![](assets/object_list.png)

1. For [!DNL Name], type a unique name for the object.

   Every object and group must use a unique name. If you created an object from the template, a default name appears. 

1. Check the following option if appropriate:

   No [!DNL Texture] for planar objects that receive color only, but will support [reflection](../../c-vat-refl-pg/c-vat-abt-refl-pg/c-vat-abt-refl-pg.md#concept-ff491f2f926e4389afac1d2e261b2e81). 

1. Click **[!UICONTROL OK]**.
1. If you ever need to change the object properties you just set, right click the object in the [!DNL Object Explorer] and choose **[!UICONTROL Properties]**.
Once you have created your hierarchy, use the [!DNL Mask] page to [define the object surfaces](../../c-vat-work-mask-pg/c-vat-create-mask/t-vat-add-mask.md#task-f8d4ae100d834ace9f90f7f260bf15aa). 
