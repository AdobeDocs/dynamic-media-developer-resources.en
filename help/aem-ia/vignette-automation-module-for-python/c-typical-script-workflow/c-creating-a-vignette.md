---
description: Once the relevant images and data are available, the next step is to create a new vignette.
seo-description: Once the relevant images and data are available, the next step is to create a new vignette.
seo-title: Create a Vignette
title: Create a Vignette
uuid: 487df9c9-0e2b-45ba-905e-6cfba479dad5
index: y
internal: n
snippet: y
---

# Create a Vignette{#create-a-vignette}

Once the relevant images and data are available, the next step is to create a new vignette.

For example:

```
>>> from s7vampy import *
>>> v = create_vignette(open_image("view-image.png"))
>>> v.view.illum[0] = open_image("view-illum.png")
>>> v.save("new-vignette.vnt")
```

This is the minimum required to build a valid vignette. The resulting vignette has a view that uses [!DNL view-image.png] as the view image and [!DNL view-illum.png] as the illumination map. The vignette also has a background object called unmasked, which masks the entire view because no other objects have been added.

It is possible at this point to associate at most three illumination maps with the view, at index 0, 1, and 2. 
