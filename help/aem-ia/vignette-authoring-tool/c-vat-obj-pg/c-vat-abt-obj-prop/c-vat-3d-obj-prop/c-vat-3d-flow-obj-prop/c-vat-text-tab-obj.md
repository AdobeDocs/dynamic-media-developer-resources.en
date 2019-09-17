---
description: null
seo-description: null
seo-title: Texture tab for objects
solution: Experience Manager
title: Texture tab for objects
topic: Scene7 Image Authoring
uuid: 7669d291-62fa-48ad-b4b7-c06c6933c55f
---

# Texture tab for objects{#texture-tab-for-objects}

This tab of the [!DNL Properties] dialog box displays the attributes of the texture space for this object. Dimensions assume that you are looking at the object head-on, viewing a flat rectangle.

**Overall Object Size:** The physical (real-life) size of the flattened object surface.

**Optimal Resolution:** A calculated value that translates the physical size of the surface to the rendering surface. This value is given in pixels per inch. When applying textures to this object, best results are achieved if the texture's resolution is the same or higher than the value shown here.

** Origin: ** The choices in this drop-down list are determined by the [origins] section of the [!DNL vat.ini]file. You can have a total of up to six user defined origins, but origin 2 must always be skipped. The entry in the first position in the [!DNL vat.ini] file is the default choice in the drop-down list. Choose an origin from the list and define it by positioning the origin manually on the selected object. The origin value is in inches relative to the top, left corner of the texture space.

The following settings affects [decals](../../../../c-vat-rend-pg/c-vat-rend-obj/c-vat-decals/t-vat-app-decal.md#task-16ff67be05f84b06b4c0caf73ff01f83) (single-repeat, flat objects that are applied on top of a material, for example logos, area rugs, embroidery, and so forth).

**Anchor Point:** Determines the origin for the decal you apply, relative to the standard texture origin of the texture beneath it.

** Light Vector Angles:** The horizontal and vertical angles for the drop shadow of the decal, if you specify one.

If you set Vert to zero, you see no drop shadow (light falls directly down on the object). Larger Vert values cause longer drop shadows. Vert must not be equal to or larger than 90 degrees.

Horiz determines the angle from which the shadow appears. Set it to zero to set the shadow parallel to the primary [texture direction](../../../../c-vat-flow-pg/c-vat-flow-mesh-tech/t-vat-change-dir-text.md#task-3f7c354a11f641738135faf7ce3fc46f). 
