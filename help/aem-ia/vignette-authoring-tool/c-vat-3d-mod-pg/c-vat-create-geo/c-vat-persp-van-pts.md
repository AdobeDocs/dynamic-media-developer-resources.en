---
description: A camera converts a real-world, three-dimensional scene into a flat, two-dimensional photograph.
seo-description: A camera converts a real-world, three-dimensional scene into a flat, two-dimensional photograph.
seo-title: About Perspective, Scene Directions, and Vanishing Points
solution: Experience Manager
title: About Perspective, Scene Directions, and Vanishing Points
topic: Scene7 Image Authoring
uuid: 100a0a5c-894a-402a-8ac5-ae0e3570c46c
---

# About Perspective, Scene Directions, and Vanishing Points{#about-perspective-scene-directions-and-vanishing-points}

A camera converts a real-world, three-dimensional scene into a flat, two-dimensional photograph.

The [!DNL Camera] tool on the [!DNL 3D Modeling] page [creates a camera model](../../c-vat-3d-mod-pg/c-vat-create-geo/t-vat-cam-mod.md#task-fc39ab753bb248c7a8f86fb27594412e) for [!DNL Image Authoring] based on the way that straight lines and edges in the real world translate to lines in the photograph.

A camera creates a perspective projection of the real 3D world:

* In the projection, objects of the same size appear larger when they are close and smaller when they are distant. 
* Straight lines in the scene remain straight lines in the projection. 
* Parallel lines in the scene intersect at a common point in the projection.

For example, all vertical lines in the scene become straight lines in the photograph and (when extended) all intersect at the same point. The intersection point is called the vanishing point, because the lines appear to vanish into it.

Vanishing points may not be visible within the bounds of the photograph. In fact, a vanishing point may be at infinity. If the vanishing point is at infinity, the projected lines are parallel in the photograph as well as in the scene. This can happen in the case of vertical elements when the scene is photographed with a perfectly level camera.

[!DNL Image Authoring] determines the position and orientation of the camera that was used to take the photograph, as well as the camera's field of view, based on your identification of three mutually perpendicular directions in the scene, which in turn define the vanishing points.

The three mutually perpendicular directions are called scene directions, and are a property of the scene content, rather than of the photograph. In other words, if you know that two items in the scene are perpendicular in real life, you identify them as such, even if they don't appear perpendicular in the photograph.

When identifying the scene directions, keep in mind the following:

* Scene directions that use strong, distinct, well-separated edges in the photograph produce a more accurate camera model. 
* The three scene directions include one vertical direction and two that lie in the horizontal plane. 
* The vertical directions correspond to natural verticals, such as the vertical edges of walls or the sides of kitchen units. 
* The horizontal edges correspond to the intersection edges of walls and ceilings or floors, or to the edges of horizontal elements, such as countertops. 
* One of the horizontal directions is generally considered the left-right direction (with respect to the photograph) and the other the in-out direction.

Some scenes may provide several candidate pairs of perpendicular horizontal directions. When choosing the best pair, bear in mind the following:

* Horizontal edges need only be perpendicular to each other-they do not need to be perpendicular to the camera in any sense. 
* Scene edges do not have to create an actual corner in order for you to use them to identify scene directions. It is sufficient that they would form a corner if they were extended.

The three scene directions you identify form a rectangular block within the scene. 
