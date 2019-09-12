---
description: For each component of your cabinet style, you must define the vertical and horizontal segments as being fixed or scaled.
seo-description: For each component of your cabinet style, you must define the vertical and horizontal segments as being fixed or scaled.
seo-title: Defining Cabinet Segments
solution: Experience Manager
title: Defining Cabinet Segments
topic: Scene7 Image Authoring
uuid: 7e1c1c97-0e10-4dfe-bf7b-f38515802c4c
index: y
internal: n
snippet: y
---

# Defining Cabinet Segments{#defining-cabinet-segments}

For each component of your cabinet style, you must define the vertical and horizontal segments as being fixed or scaled.

The panels that form the perimeter of the cabinet are defined as fixed, and the center panel is defined as scaled. When you insert the cabinet into an [!DNL Image Authoring] vignette, the perimeter segments snap to the edges of the space defined for that cabinet door, and the center panel will scale to fill the remaining space.

**To Define a Cabinet Component Segment:** 

1. Under [!DNL Segment], click one of the following:

    * **[!UICONTROL Horizontal]** defines segments from the left side of the component to the right side of the component. 
    * **[!UICONTROL Vertical]** defines segments from the top of the component to the bottom of the component.

1. Click **[!UICONTROL First]**.
1. Click the point where the first segment should end. (The edge of the component is automatically defined.)

   For example, if your cabinet style has a border, click at the inmost edge of that border. If you click the wrong spot, just click again until the blue line defines the border correctly. The old line disappears each time you click a new location. 

1. Click **[!UICONTROL Fixed]** or **[!UICONTROL Scale]**.

   The segments that form the border of the cabinet should be fixed and the center area should be scaled. Do not choose any of the other choices under [!DNL Type]. 

1. Click **[!UICONTROL Second]**.
1. Click the point where the second segment should end.

   For example, if the second segment is the center of the cabinet door, click at the far edge of that panel. 

1. Click **[!UICONTROL Fixed]** or **[!UICONTROL Scale]**.
1. Click **[!UICONTROL Third]**.

   If this is the final segment you are defining, you should see a blue line at the far edge of your cabinet. If there is a value (other than zero) for Width (pixels) at the bottom of the [!DNL Segment] area, then this segment is already defined. 

1. Click **[!UICONTROL Fixed]** or **[!UICONTROL Scale]**.
1. Select any remaining segment choices (for example, Fourth and Fifth) if you are not using them, then click **[!UICONTROL Delete Segment]** for each one.
1. Type a resolution for this cabinet component.

   This value cannot be zero. You may need to experiment to find the right resolution for your image. If, when you apply the cabinet in [!DNL Image Authoring], the border segments are too thin, you need to make the resolution value smaller. If you don't know the correct number of pixels per inch represented by your image, try using a value of 18. 

1. If necessary, check **[!UICONTROL Texturable]**.

   If this image contains alpha channels, checking this setting lets you apply textures to the cabinet in [!DNL Image Authoring]. If the image does not contain alpha channels, checking this box has no effect. If the image contains alpha channels but you do not check this setting, you can apply stains to the image (you can colorize it), but you cannot apply textures. 

1. Repeat these steps for each [component](../../c-cat-about-cat/c-cat-creating-cabinet-files/t-cat-cabinet-comp.md#task-fcd047f1ea13431ea26de2f9d22ed81f) in your cabinet style.
