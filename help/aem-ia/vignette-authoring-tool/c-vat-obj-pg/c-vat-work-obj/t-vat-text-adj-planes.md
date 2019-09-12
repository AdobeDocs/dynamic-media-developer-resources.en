---
description: You may want textures on adjacent planes in a 3D vignette to align so that, for example, wallpaper flows across wall intersections properly.
seo-description: You may want textures on adjacent planes in a 3D vignette to align so that, for example, wallpaper flows across wall intersections properly.
seo-title: Matching Up Textures on Adjacent Planes
solution: Experience Manager
title: Matching Up Textures on Adjacent Planes
topic: Scene7 Image Authoring
uuid: 789719e4-8d35-4b3a-9c46-18122af3a2c0
index: y
internal: n
snippet: y
---

# Matching Up Textures on Adjacent Planes{#matching-up-textures-on-adjacent-planes}

You may want textures on adjacent planes in a 3D vignette to align so that, for example, wallpaper flows across wall intersections properly.

When you match textures across adjacent walls, choose any prominent wall as a starting point, and place the [origin](../../c-vat-rend-pg/c-vat-work-text/c-vat-abt-origin.md#concept-643d030b62fd42a5bf3ce4e4ab9a3a47) in one of the corners. Use the [!DNL Match Origin] command to connect adjacent walls, continuing across the room until all walls have been connected. Apply a wallpaper on the [ [!DNL Render] page](../../c-vat-rend-pg/c-vat-abt-rend-pg/c-vat-abt-rend-pg.md#concept-0a56eec3cafe45658d25c0988d818fc0) to verify.

When you match textures across adjacent countertops, start with one of the tops and position the origin in a corner. Use the [!DNL Match Origin] command to connect adjacent surfaces (backsplashes, edges), until all counter surfaces have been connected. Apply a tile texture on the [!DNL Render] page to verify. You may need to make small adjustments to get the grout of the first run of tiles at the front edges to cleanly align with the edge of the counter.

This command may place the origin outside the object area-this is expected behavior.

**To Match Up Textures on Adjacent Planes:** 

1. Make sure all [texture directions](../../c-vat-obj-pg/c-vat-obj-pg-tools/c-vat-align-tool.md#concept-2ba104eab0df4b00a52c70bbcd8177a8) run left to right using the [!DNL Alignment] tool.
1. With the [!DNL Alignment] tool still selected, click the object that is the most prominent (of the ones you're aligning). For example, if you are aligning three walls, choose the one that displays the most texture when it is rendered.
1. Set the texture origin by clicking the object where you want the [texture anchor point](../../c-vat-obj-pg/c-vat-obj-pg-tools/c-vat-layout-tool/t-vat-chg-anchor-pt.md#task-cb8a0e9f062f4bfbb4fb730d08f86ddb) to appear.

   The direction of the line that appears from the point you clicked indicates the horizontal orientation of the texture. 

1. Hold down the Alt key and click to select an adjacent planar object.
1. Right-click and choose **[!UICONTROL Match Origin]**.
1. In the list that appears, select the previously-selected planar object.
1. Repeat steps 4-6 for the other adjacent planes you want to align.

   When you select from the [!DNL Match Origin] list, always select an adjacent planar object whose origin has already been set. This can cause the origin for some planes to move outside their objects, but don't adjust the resulting origins. 

