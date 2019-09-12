---
description: A vignette view or overlapping object can have at most three illumination maps.
seo-description: A vignette view or overlapping object can have at most three illumination maps.
seo-title: class s7vampy.illum.IlluminationMaps(view)
title: class s7vampy.illum.IlluminationMaps(view)
uuid: 7a5caf84-4eb7-4568-8faf-fdb02a8fea49
index: y
internal: n
snippet: y
---

# class s7vampy.illum.IlluminationMaps(view){#class-s-vampy-illum-illuminationmaps-view}

A vignette view or overlapping object can have at most three illumination maps.

Vignettes contain two types of illumination maps:

* Global illumination maps, associated with a vignette view. 
* Local illumination maps, associated with an overlapping object.

Illumination maps are accessed through the `illum` property available for both ` [s7vampy.view.View](../../../c-s7vampy-api-reference/c-classes/c-view/r-s7vampy-view-view.md#reference-6183812d68624a6b803fb175e237c6f8)` and [overlapping object](../../../c-s7vampy-api-reference/c-classes/c-objects/r-class-s7vampy-obj-staticoverlapobject.md#reference-7b66780df1fc40cfa436fecdc16037c5) instances.

Illumination maps that are associated with a vignette view or overlapping object must be the size of the vignette view.

A vignette view must have at least one illumination map associated with it, otherwise ` [s7vampy.vignette.Vignette.save()](../../../c-s7vampy-api-reference/c-classes/c-vignette/r-class-s7vampy-vignette-vignette.md#reference-b63a48cb2bd04a1d98930e059a0f3678)` raises an exception.

The `IlluminationMaps` class provides the following capabilities:

* `len(illum)` returns the number of illumination maps (always 3) 
* Iterate over the illumination maps. Always returns three illumination maps, of which any one of them might be None. 
* Array index support, for instance `illum[0]` returns the first illumination map (illumination map A).

## Typical Use Cases {#section-6923c83094614106af6f7c114c156f18}

**Retrieve an illumination map from a view:**

```
>>> from s7vampy import *
>>> v = open_vignette("TestData/vignette.vnt")
>>> illum_a = v.view.illum[0]
>>> illum_a
```

**Associate an illumination map with a view:**

```
>>> from s7vampy import *
>>> v = open_vignette("TestData/vignette.vnt")
>>> view.illum[0] = open_image("TestData/illum.png")
>>> view.illum[0]
```

**Remove an illumination map from a view:**

```
>>> from s7vampy import *
>>> v = open_vignette("TestData/vignette.vnt")
>>> del v.view.illum[0]
>>> v.view.illum[0]
None
```

**Alternative way to remove an illumination map from a view:**

```
>>> from s7vampy import *
>>> v = open_vignette("TestData/vignette.vnt")
>>> v.view.illum[0] = None
>>> v.view.illum[0]
None
```

