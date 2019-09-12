---
description: Base class of all objects and object groups that are stored in the object hierarchy.
seo-description: Base class of all objects and object groups that are stored in the object hierarchy.
seo-title: class s7vampy.obj.Object(parent, obj)
title: class s7vampy.obj.Object(parent, obj)
uuid: 60663183-9414-4e68-93da-e3e1af1b1615
index: y
internal: n
snippet: y
---

# class s7vampy.obj.Object(parent, obj){#class-s-vampy-obj-object-parent-obj}

Base class of all objects and object groups that are stored in the object hierarchy.

Use one of the following attributes to determine the type of the object:

* [is_group](../../../c-s7vampy-api-reference/c-classes/c-objects/r-class-s7vampy-obj-group.md#reference-d4268759bb7740659019fec3eb7cbe91) 
* [is_background_object](../../../c-s7vampy-api-reference/c-classes/c-objects/r-class-s7vampy-obj-backgroundobject.md#reference-e6a4e2d3c1f2458e8fbdcc290d20dd14) 
* [is_static_object](../../../c-s7vampy-api-reference/c-classes/c-objects/r-class-s7vampy-obj-staticobject.md#reference-bd09110f7ce04b6d88fdf1c5f1a72804) 
* [is_static_overlap_object](../../../c-s7vampy-api-reference/c-classes/c-objects/r-class-s7vampy-obj-staticoverlapobject.md#reference-7b66780df1fc40cfa436fecdc16037c5) 
* [is_nontexturable_object](../../../c-s7vampy-api-reference/c-classes/c-objects/r-class-s7vampy-obj-nontexturableobject.md#reference-161cbb70e49e47ed908036ec35db68cc) 
* [is_surface_object](../../../c-s7vampy-api-reference/c-classes/c-objects/r-class-s7vampy-obj-surfaceobject.md#reference-cf2b73b972e84cf5b9a0e22ab3d106f4) 
* [is_flat_object](../../../c-s7vampy-api-reference/c-classes/c-objects/r-class-s7vampy-obj-flatobject.md#reference-e6da5ec8f3564cd088891e6c64205552)

Use the ` [is_overlapping_object](../../../c-s7vampy-api-reference/c-classes/c-objects/r-class-s7vampy-obj-staticoverlapobject.md#reference-7b66780df1fc40cfa436fecdc16037c5)` attribute to determine whether the object is an overlapping object. A non-static overlapping object has its own set of local illumination maps. These can be accessed using the `illum` attribute.

All overlapping objects have a z-order associated with them. The z-order determines the order in which the overlapping objects are drawn. Objects with a high z-order are drawn later, in front of objects with a low z-order.

Not all object types are supported by the Vignette Automation Module. Unsupported objects can be detected using the `is_supported` attribute.

<table id="table_29593A7DCCE443CFA4B23D8D5A2CBDED"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Attribute </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> is_background_object</span> </p> </td> 
   <td colname="col2"> <p>True if this object is a background object. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> is_flat_object</span> </p> </td> 
   <td colname="col2"> <p>True if this object is a flat model object. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> is_group</span> </p> </td> 
   <td colname="col2"> <p>True if this object is an object group. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> is_nontexturable_object</span> </p> </td> 
   <td colname="col2"> <p>True if this object is a non-texturable object. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> is_overlapping_object</span> </p> </td> 
   <td colname="col2"> <p>True if this object is an overlapping object </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> is_static_object</span> </p> </td> 
   <td colname="col2"> <p>True if this object is a static object. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> is_static_overlap_object</span> </p> </td> 
   <td colname="col2"> <p>True if this object is a static overlap object. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> is_supported </span> </p> </td> 
   <td colname="col2"> <p>True if this object is a supported object type. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> is_surface_object</span> </p> </td> 
   <td colname="col2"> <p>True if this object is a surface model object. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> name</span> </p> </td> 
   <td colname="col2"> <p> Object or object group name </p> <p>[str] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parent</span> </p> </td> 
   <td colname="col2"> <p>Parent object group (Group or None). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> path</span> </p> </td> 
   <td colname="col2"> <p>Slash-separated path to this object or group in the hierarchy </p> <p>For example: <span class="codeph"> group1/group2/object</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

