---
description: You can apply textures to objects in your vignette from the IPS (Image Production System) or from Windows Explorer.
seo-description: You can apply textures to objects in your vignette from the IPS (Image Production System) or from Windows Explorer.
seo-title: Dragging and Dropping Textures
solution: Experience Manager
title: Dragging and Dropping Textures
topic: Scene7 Image Authoring
uuid: 605cdb2d-c6ac-4979-b627-b06359906295
index: y
internal: n
snippet: y
---

# Dragging and Dropping Textures{#dragging-and-dropping-textures}

You can apply textures to objects in your vignette from the IPS (Image Production System) or from Windows Explorer.

In order to do this, you must configure the [!DNL Material Drag & Drop Behavior] settings on the [!DNL Preferences] dialog box.

The textures you apply in this way are listed on the [ [!DNL Material History]](../../c-vat-rend-pg/c-vat-rend-tools/t-vat-mat-hist-tool.md#task-95e1391588974719bbf93850448d547b) list and may be added to the [ [!DNL Favorite Materials]](../../c-vat-rend-pg/c-vat-rend-tools/c-vat-fav-mat-tool/t-vat-fav-mat-list.md#task-488e210530c24f6bbf7b37d0b6109b61) or [ [!DNL Saved Materials]](../../c-vat-rend-pg/c-vat-rend-tools/t-vat-saved-mat-tool/t-vat-saved-mat-tool.md#task-2f7dd900c44e42f4a8e7f41a3003e2fa) lists, where you can re-use them for any object in the vignette. (To have [!DNL Image Authoring] add materials to the [!DNL Saved Materials] list automatically, check the [!DNL Save material to vignette] checkbox on the [!DNL Render Page] tab of the [!DNL Preferences] dialog box. See step 1, below.)

Textures you apply from the IPS server are available only when your computer can connect to it.

You also may need to [prepare the images you plan to drag and drop from IPS](../../c-vat-rend-pg/c-vat-rend-obj/r-vat-ips-drag-drop.md#reference-963dec714cc84ce4ae99d6e7ad960b9d). If you plan to apply a decal from IPS, the decal image must have a user-defined field called "Repeat" that has a value of "14." If you plan to apply a border from IPS, the border must have a user-defined field called "Repeat" that is set to a value of "12."

**To Drag and Drop Textures:** 

1. [Configure the [!DNL Material Drag & Drop Behavior] settings](../../c-vat-rend-pg/c-vat-abt-rend-pg/c-vat-rend-pg-pref.md#concept-158b19aeeda74bb28fcac3b684ca1efc) on the [!DNL Render Page] tab of the [!DNL Preferences] dialog box.
1. Click the **[!UICONTROL Render Page]** button ![](assets/render.png).
1. Display the IPS [!DNL Browse Images] page or the folder containing your texture file in Windows Explorer.

   To display the [!DNL Browse Images] page, start your Internet browser and navigate to the IPS. Log in and display the appropriate samples in the [!DNL Browse Images] page. 

1. If you need to select an object before applying the texture, click back in [!DNL Image Authoring] and choose the object or group for this texture.

   Select an object or group from the [ [!DNL Select Object] box](../../c-vat-gs/c-vat-sel-obj/c-vat-sel-object-box.md#concept-d127c6efaabd436a96c02f36a7bce6ac), or click the item you want. Click once to select the group. If it has sub-groups, each additional click selects the subordinate group until you reach the object. At that point, additional clicks cycle back until you reach the group level.

   If you use the mouse-click method, check the [!DNL Select Object] box to see what's selected. If you are applying a decal, select a single object (not a group). If you are applying a border to a wall, select sub-selections. 

1. Drag the texture you want from the IPS [!DNL Browse Images] page or Windows Explorer to the [!DNL Image Authoring] window.
1. Release the mouse button in the [!DNL Image Authoring] window.

   Depending on how you specified drag and drop behavior for [!DNL Render Page Preferences], the texture is either applied to the selected object or to an object you choose from a pop-up menu when you drop the texture on your vignette. Textures you dragged and dropped from IPS display a lowercase "i" in front of their names. 

