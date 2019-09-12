---
description: Websites that support dynamic rendering lets end-users interactively decorate vignettes.
seo-description: Websites that support dynamic rendering lets end-users interactively decorate vignettes.
seo-title: About Dynamic Rendering
solution: Experience Manager
title: About Dynamic Rendering
topic: Scene7 Image Authoring
uuid: cb8d28ca-832c-42db-adc3-498c0043c86c
index: y
internal: n
snippet: y
---

# About Dynamic Rendering{#about-dynamic-rendering}

Websites that support dynamic rendering lets end-users interactively decorate vignettes.

A simple implementation might let the end-user apply one of a thousand fabrics to a sofa or a shirt. In this case, the fabric is applied to the entire vignette.

A more complex implementation would let the end-user apply fabrics or other finishes to individual areas within the vignette. For example, the end-user could try out one fabric on a shirt, another on a jacket, and a third on a skirt. This technique can be applied to room scenes as well as apparel. For example, a kitchen scene might let the end-user apply tiles or granite to a countertop, wood or linoleum to the floor, and wallpaper or paint to the walls.

If you plan to create images that are dynamically rendered on your website, you need to plan your vignettes accordingly. It is important to work with your Web development group to understand how the vignettes are used on the website.

When images are dynamically rendered on a website, the render server uses the image hierarchy to determine which objects in the vignette can be decorated. In simple implementations, every masked object that is part of a group is decorated. In complex implementations, groups and sub-groups can be decorated separately. 
