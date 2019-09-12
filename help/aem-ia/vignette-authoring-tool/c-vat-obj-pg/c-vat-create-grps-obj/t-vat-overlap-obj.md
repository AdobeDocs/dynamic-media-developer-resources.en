---
description: Overlap objects have z-order values, which determine where each one appears in a stack of objects.
seo-description: Overlap objects have z-order values, which determine where each one appears in a stack of objects.
seo-title: Creating Overlap Objects
solution: Experience Manager
title: Creating Overlap Objects
topic: Scene7 Image Authoring
uuid: ee8b75e0-2209-4676-baa6-7def5a3c9227
index: y
internal: n
snippet: y
---

# Creating Overlap Objects{#creating-overlap-objects}

Overlap objects have z-order values, which determine where each one appears in a stack of objects.

The higher the z-order value, the higher the object is in the stack (the closer it is to the viewer). No two overlap objects within a single vignette should use the same z-order value.

You cannot create overlap objects directly, but you can convert any 3D object to an overlap object type.

You can re-use overlap objects in other vignettes by exporting and then importing them. You can move overlap objects on the [!DNL Render] page.

**To Create Overlap Objects:** 

1. Determine the desired z-order for all overlapping objects that appear in your vignette.
1. Create a separate, temporary, 3D vignette, using the same image that you use in your final vignette.
1. In the temporary vignette, go to the [!DNL Object] page and create the groups and objects that become your overlap objects.
1. Right-click each of these objects and choose **[!UICONTROL Convert to]** > **[!UICONTROL Renderable Overlap Object or Convert to]** > **[!UICONTROL Static Overlap Object]**.

   A renderable object can accept textures and colors. A static object cannot. You may want to include static items in a vignette to demonstrate object scale or to decorate a scene.

   As you convert each object, its [!DNL Object Properties] dialog box displays. Specify the z-order value for each object, making sure that each object's z-order value is unique and that these values reflect your desired z-order for all the objects (with 0 being the furthest away from the viewer). 

1. Save and close the temporary vignette. Remember to use a different filename than your master vignette uses.
1. Open the vignette that uses the overlap objects (the master vignette).
1. On the [!DNL Object] page, right-click the vignette name in the [!DNL Object Hierarchy], then choose **[!UICONTROL Open Import Vignette]**.
1. Select the temporary vignette and click **[!UICONTROL OK]**.
1. Right-click the vignette name again.

   On the list of groups you can create, you can see the groups from your temporary vignette. 

1. Choose one of the groups representing the overlap objects you want to import.
1. Right-click the new group and choose the objects comprising that group.
1. Repeat steps 9-11 for each overlap object, then right-click the vignette name again and choose **[!UICONTROL Close Import Vignette]**.
