---
title: Example C
description: Create a "paper doll" layering application.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 70232055-2a4c-4e56-8076-3cd56a9004c5
---
# Example C{#example-c}

Create a "paper doll" layering application.

 A background image contains the photo of a model or mannequin. Additional records in the image catalog contain various apparel and accessory items, photographed to match the mannequin in shape and size.

Each apparel/accessory photo is masked and cropped to the mask bounding box to minimize the image sizes. Image anchors and resolutions are carefully controlled to maintain alignment between the layers and the background image, and all images are added to an image catalog, with the appropriate values stored in `catalog::Resolution` and `catalog::Anchor`.

In addition to layering, you also want to change the color for selected items. The records for these items are preprocessed to remove the original color and adjust the brightness and contrast in a fashion suitable for the colorizing command. This preprocessing might be done off-line, using an image editing tool such as Adobe Photoshop, or, in simple cases, it can be done trivially by adding `op_brightness=` and `op_contrast=` to the `catalog::Modifier`field.

This application does not warrant a separate template, because all objects are already properly aligned by their image anchors ( `catalog::Anchor`), and scaled ( `catalog::Resolution`). It is left up to the client to ensure appropriate layer order.

A typical request might look like this:

```
http://server/rootId/mannequin?&hei=400&qlt=90&
layer=1&res=999&src=rootId/tankTopGeneric&colorize=240,122,17&
 layer=2&res=999&src=rootId/skirt14a&
layer=3&res=999&src=rootId/jacket09&
layer=4&res=999&src=rootId/hat2generic&colorize=12,15,34&
 layer=5&res=999&src=rootId/sunglasses&
layer=6&res=999&src=rootId/shoes21
```

Only the height is specified. Doing so allows the returned image to vary in width depending on the aspect ratio of the mannequin image, without getting margins filled with the background color.

It should not matter what resolution is specified for each layer, as long as they are all the same. This version may not allow views to be larger than the composite images. Specifying a large resolution value avoids problems related to this limitation. All processing and compositing is done at the optimal resolution for the requested image size, to help achieve best performance and output quality.

The `res=` commands can be omitted if all source images have the same resolution at full scale (which is likely the case for this type of application).

The `rootId` must be specified for all `src=` commands, even if they are the same as the `rootId` specified in the url path.

If no image catalog is to be used, a resolution-based approach to scaling is not possible. In this case, explicit scale factors must be calculated for each layer item, based on the ratio of the `catalog::Resolution` values for each layer to the `catalog::Resolution` value of the background layer. The compositing request (with fewer layers) might thus look like this:

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```
