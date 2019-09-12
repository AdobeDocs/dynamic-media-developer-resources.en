---
description: When you apply textures to objects in Image Authoring, you mirror the real-world work of wallpaperers, tilesetters, countertop installers, upholsterers, and apparel designers.
seo-description: When you apply textures to objects in Image Authoring, you mirror the real-world work of wallpaperers, tilesetters, countertop installers, upholsterers, and apparel designers.
seo-title: Aligning Textures to Objects
solution: Experience Manager
title: Aligning Textures to Objects
topic: Scene7 Image Authoring
uuid: 39d4424f-f516-437f-a769-094d1439028c
index: y
internal: n
snippet: y
---

# Aligning Textures to Objects{#aligning-textures-to-objects}

When you apply textures to objects in Image Authoring, you mirror the real-world work of wallpaperers, tilesetters, countertop installers, upholsterers, and apparel designers.

Your approach to making the applied texture align properly with its object varies, depending on the following:

* **The Type of the Object** When you apply wallpaper to a wall, you apply the paper vertically, but you can start at any point on the wall and it usually doesn't matter which part of the paper aligns with the top or bottom of the wall. For countertops, however, to avoid excessive cutting you would place the first whole tile at the upper left corner of the counter or backsplash. When you apply upholstery to furniture, the alignment of the fabric may depend on the pattern or the shape of the object.

* **Whether the Object Consists of One or Multiple Parts** For objects with more than one renderable surface, you may need to flow the material smoothly and continuously across the surface. For example, you may need to wrap wallpaper or a border across two or more adjacent walls; align tiles across a countertop, edge, and backsplash; or apply fabric continuously across the seat back, seat cushions, and front skirt of an upholstered chair.

* **The Contents of the Material's Texture Image** It is easier to apply texture images for materials with no discernible patterns (laminate, concrete, carpet, solid fabrics) than to apply materials that have a strong, repeated pattern.

  When you author a scene in [!DNL Image Authoring], you may not know what material will be applied. When production assistants create repeatable textures, they may not know to which objects the material will be applied. [!DNL Image Authoring] lets you define separate alignment points for objects (the [texture origin](../../c-vat-rend-pg/c-vat-work-text/c-vat-abt-origin.md#concept-643d030b62fd42a5bf3ce4e4ab9a3a47)) and for repeatable textures (the [texture anchor point](../../c-vat-rend-pg/c-vat-work-text/t-vat-text-anchor-pt.md#task-b74408a9bc9641a090d89e8966e4587b)) to give you maximum control for aligning the two. When you apply a texture to an object, the texture anchor point matches up with the origin to position the texture on the object's surface.

