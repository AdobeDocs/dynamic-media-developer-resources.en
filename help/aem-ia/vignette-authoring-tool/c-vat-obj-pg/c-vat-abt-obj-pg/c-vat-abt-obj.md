---
description: An object is a particular area of the photo that you can decorate.
seo-description: An object is a particular area of the photo that you can decorate.
seo-title: About Objects
solution: Experience Manager
title: About Objects
topic: Scene7 Image Authoring
uuid: 008ec9f0-71b5-45e7-a07b-ffe0838887b5
---

# About Objects{#about-objects}

An object is a particular area of the photo that you can decorate.

For example, in a photo containing a wall and a floor, the wall might be an object. When a customer clicks the wall, then clicks a wallpaper sample, the wallpaper appears on the wall only. You create a wall object that defines the wall as the area that receives wallpapers.

More complex items may contain multiple objects. You create multiple objects for an item when you want to apply patterns to the item. Patterns appear differently, depending on the shape and angle of the object to which they are applied.

For example, if your image contains a sofa, but you want to change only the color of the sofa, you can make the whole sofa a single object. When you click anywhere in the sofa, then click a color sample, the whole sofa changes color.

If you want to apply a patterned fabric to the sofa, you would define the arms, cushions, back, and so on, as separate objects. The same fabric appears on the whole sofa, but it looks one way on a cushion and another way when stretched around the arms.

You can make an object renderable or static. A renderable object can accept textures and colors. A static object cannot. You may want to include static items in a vignette to demonstrate object scale or to decorate a scene. You cannot create a static object, but you can [convert](../../c-vat-obj-pg/c-vat-work-obj/t-vat-chg-obj-type.md#task-ce743f3c8ab74682abd1841e340a9e66) most objects to a static type.

You can convert an object to an [overlap object type](../../c-vat-obj-pg/c-vat-create-grps-obj/t-vat-overlap-obj.md#task-444f7cb2256040a48ba41ce380348465). This object type has a z-order value, which determines where it appears in a stack of objects. The higher the z-order value, the higher the object is in the stack. No two overlap objects within a single vignette should use the same z-order value.

You can create a special type of overlap object called a [highlight matte object](../../c-vat-work-mask-pg/c-vat-create-mask/t-vat-high-matte-obj.md#task-a999ee1887384d16ba39dc763ed0c774). This object lets you create an illumination map for glossy materials, such as metallic finishes or patent leather. It is intended for use in vignettes that show individual product shots, and not room scenes. Once you have a highlight matte object, you use tools on the [!DNL Mask] page and the [!DNL Illumination] page to create the highlights. 

>[!MORELIKETHIS]
>
>* [Changing an Object's Type](../../c-vat-obj-pg/c-vat-work-obj/t-vat-chg-obj-type.md#task-ce743f3c8ab74682abd1841e340a9e66)
>* [Copying an Object](../../c-vat-obj-pg/c-vat-work-obj/t-vat-copy-obj.md#task-0b0582d7480a4d6991278ecb688c7823)
>* [Creating 2D Objects](../../c-vat-obj-pg/c-vat-create-grps-obj/t-vat-create-2d-obj.md#task-b0c168d6f127408c882e8f1de36c8bc7)
>* [Deleting a Group or Object](../../c-vat-obj-pg/c-vat-work-obj/t-vat-del-obj.md#task-0b06646b938043acbe4376dff2ceffcc)
>* [Moving an Object](../../c-vat-obj-pg/c-vat-work-obj/c-vat-move-obj.md#concept-adff591e78a04f0d98cfd31cc7f94eed)
