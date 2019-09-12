---
description: Use these steps to associate data with flat objects.
seo-description: Use these steps to associate data with flat objects.
seo-title: Flat Objects
title: Flat Objects
uuid: ed4d850b-3a1a-4f24-a7b5-c43a46c670a2
index: y
internal: n
snippet: y
---

# Flat Objects{#flat-objects}

Use these steps to associate data with flat objects.

1. Set the perspective quadrilateral.
1. Set the texture direction (optional).

   Step Result The perspective quadrilateral is first created as a path with four line segments. The script provides the size of the quadrilateral in inches so a texture or decal can be scaled appropriately when applied during rendering. 
>
>The initial direction of the texture on a flat object is from the first point to the second point of the quadrilateral. This can be changed if needed. 
>
>Example: 
>
>```>
>>>> from s7vampy import *
>>>> v = create_vignette(open_image("view-image.png"))
>>>> v.view.illum[0] = open_image("view-illum.png")
>>>> group = v.objects.add_group("group")
>>>> obj = group.add_flat_object("obj", open_image("obj-mask.png"))
>>>> quad = create_path()
>>>> quad.moveto(50,50)
>>>> quad.rlineto(100,0)
>>>> quad.rlineto(0,100)
>>>> quad.rlineto(-100,0)
>>>> quad.close()
>>>> obj.set_perspective(quad,5,5)
>>>> obj.rotate = 90
>>>> v.save("new-vignette.vnt")
>```>
>This script adds a new flat object that is defined by the mask `obj-mask` and the perspective quad, which is a rectangle at (50, 50) with a width and height of 100. 
>
>The texture direction, as defined by rotate, is a clockwise angle relative to the left-to-right direction. Setting the texture direction to 90 degrees flows the texture from top to bottom. 

