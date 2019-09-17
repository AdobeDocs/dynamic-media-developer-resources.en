---
description: The Trace Tool is the main tool used to create a mask.
seo-description: The Trace Tool is the main tool used to create a mask.
seo-title: The Trace Tool
solution: Experience Manager
title: The Trace Tool
topic: Scene7 Image Authoring
uuid: b4a9564f-8b9d-492c-bee4-4f44ee00ae09
---

# The Trace Tool{#the-trace-tool}

The Trace Tool is the main tool used to create a mask.

The [!DNL Trace] tool has the following options:

* **Feather:** Lets you blur the edge of a mask, like a soft brush edge setting for the [ [!DNL Mask Brush] tool](../../c-vat-work-mask-pg/c-vat-mask-pg-tools/c-vat-mask-brush.md#concept-8a63068b04084b57a4f1ed8fd27fcb72). The [!DNL Feathering range] is 0 to 10, with 10 being the softest. By default, feathering is set to 0, which turns this feature off.

You can use feathering to mask a blurred object behind the one that's in focus, or to mask the edge of a translucent item, such as a curtain.

You can also use the [ [!DNL Feather] tool](../../c-vat-work-mask-pg/c-vat-mask-pg-tools/c-vat-feather-tool.md#concept-ba004c22a35846f68396e4f527c5303e) to blur the edges of a mask after you've created it.

* **Opacity:** Lets you mask areas translucently. The [!DNL Opacity range] is 0 to 100%, with 100% (the default) being completely opaque.

You can use opacity to mask an object that is seen through a transparent or translucent area, such as a wall seen through transparent drapes or a couch behind a glass table. You use opacity when you [define the mask for a highlight matte object](../../c-vat-work-mask-pg/c-vat-create-mask/t-vat-high-matte-obj.md#task-a999ee1887384d16ba39dc763ed0c774).

* **Straight Edges:** Ensures that all new vertices are sharp and all new edges are straight, unless you choose a different vertex type from the right-click menu. Existing vertexes and edges are not changed.

When you don't check [!DNL Straight Edges] and you add a vertex in the middle of a line, you can click and drag that vertex (which is a sharp vertex). If you create a new vertex and drag, that vertex automatically becomes a smooth vertex.

* ** Hide Outline on Drag:** Turns off the display of the mask outline each time you drag the mask shape to adjust it.

Use the [!DNL Edge] tab to [define the edges of an object](../../c-vat-work-mask-pg/c-vat-create-mask/t-vat-edge-recog-masks.md#task-4fe94280df4848baae7f6c417890022a):

* **Sensitivity:** Adjusts the edge definition. Lowering the sensitivity causes only the highest-contrast areas to be defined as edges. Raising it causes more edges to appear, but they may interfere with the true edges of objects. 
* **Display:** Adjusts the appearance of edges from opaque to transparent. 
* **Recalc:** Displays the [!DNL Extract Edges] from [!DNL Image] dialog box, where you can set options for [defining default edges](../../c-vat-work-mask-pg/c-vat-create-mask/t-vat-edge-recog-masks.md#task-4fe94280df4848baae7f6c417890022a).

The right-click menu contains commands that let you choose different vertex types:

** Smooth Vertex:** A vertex with Bezier handles. The control points at the end of the Bezier handles are always equidistant from the vertex and 180 degrees from each other.

** Straight Vertex:** A vertex with Bezier handles. The control points at the end of each Bezier handle are always 180 degrees from each other and may have differing distances from the vertex.

**Corner Vertex:** A vertex with Bezier handles. The control points at the end of each Bezier handle are freeform.

**Sharp Vertex:** A vertex with no Bezier handles. This is the traditional vertex used in previous versions of [!DNL Image Authoring]. If a sharp vertex is surrounded by Bezier curves, there are no straight lines on either side of that vertex. 
