---
description: The Vignette class is the main entry point that scripts use to interact with a vignette.
seo-description: The Vignette class is the main entry point that scripts use to interact with a vignette.
seo-title: class s7vampy.vignette.Vignette(vignette)
title: class s7vampy.vignette.Vignette(vignette)
uuid: c1d3e0cd-d70c-493c-b7d9-2da6d463a121
---

# class s7vampy.vignette.Vignette(vignette){#class-s-vampy-vignette-vignette-vignette}

The Vignette class is the main entry point that scripts use to interact with a vignette.

An existing vignette can be opened using the ` [s7vampy.open_vignette()](../../../c-s7vampy-api-reference/c-functions/r-s7vampy-open-vignette.md#reference-997d6f8f0f1f4b539475a86d1fa8be81)` function. The method returns an instance of the Vignette class, which can then be used to either inspect the vignette or add more content to it.

New vignettes can be created using the ` [s7vampy.create_vignette()](../../../c-s7vampy-api-reference/c-functions/r-s7vampy-create-vignette.md#reference-86313ac79bc14fdb9e68e1138c8261e0)` function. The script is required to provide the view image, which is used to create the vignette view.

`filename [str, read-only]`

Vignette filename. May be None if the vignette has not been written to disk.

`master [bool, read-only]`

True if the vignette is a master vignette.

`objects [s7vampy.obj.ObjectHierarchy]`

Object hierarchy ( ` [s7vampy.obj.ObjectHierarchy](../../../c-s7vampy-api-reference/c-classes/c-objects/r-s7vampy-obj-objecthierarchy.md#reference-de34c2cc4dbf49e1878b190fffa646bb)`).

Use this property to find objects and object groups in the vignette or add new objects and object groups to the vignette.

`save (filename=None)`

<table id="table_423B45191C70495A8AE3AEB87E76F886"> 
 <tbody> 
  <tr> 
   <td> <b> Parameters:</b> </td> 
   <td> <p><span class="codeph"> filename (str)</span> </p> <p>Optional name of the vignette file where the vignette will be written to. </p> </td> 
  </tr> 
 </tbody> 
</table>

Save the vignette to disk.

If a filename is provided, the vignette is saved to the given filename. The behavior is the same as `Save As` in Image Authoring.

If a filename is not provided, the vignette is saved to the location where the vignette was opened or last saved. Only changed data is saved to the file in this case. The behavior is the same as `Save` in Image Authoring.

>[!NOTE]
>
>It is recommended not to overwrite vignettes. A failure in a script that updates vignettes may cause a lot of vignettes to become unusable.

`title [str]`

Vignette title.

`version [int, read-only]`

Vignette version.

`view [s7vampy.view.View]`

Vignette view ( ` [s7vampy.view.View](../../../c-s7vampy-api-reference/c-classes/c-view/r-s7vampy-view-view.md#reference-6183812d68624a6b803fb175e237c6f8))`.

Use this property to access the vignette view, its properties, and the illumination maps associated with the vignette view. 
