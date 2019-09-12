---
description: Object groups usually contain one or more objects or object groups. Object groups are used to build the object hierarchy of a vignette.
seo-description: Object groups usually contain one or more objects or object groups. Object groups are used to build the object hierarchy of a vignette.
seo-title: class s7vampy.obj.Group(factory, parent, obj)
title: class s7vampy.obj.Group(factory, parent, obj)
uuid: 07b8d1ce-e346-494e-9b5a-5d4436261ce7
index: y
internal: n
snippet: y
---

# class s7vampy.obj.Group(factory, parent, obj){#class-s-vampy-obj-group-factory-parent-obj}

Object groups usually contain one or more objects or object groups. Object groups are used to build the object hierarchy of a vignette.

Derived from [Object](../../../c-s7vampy-api-reference/c-classes/c-objects/r-class-s7vampy-obj-object.md#reference-6b1486208ad24966b84942e03e5ae9ad).

Object groups can also be used to make it easy to apply the same material to multiple objects in a vignette.

For instance if you have a shirt that is built up from multiple masks you could end up with the following hierarchy:

* shirt

    * left 
    * right 
    * collar

When you render the vignette on a server or using the render page in Image Authoring, you can apply a material to the shirt group, which applies that material to the individual objects.

` add_flat_object ( *`name`*, *`mask`*, *`*_`*, *`**keywords`*)`

<table id="table_486A1146171F418B804C25BDFE35F350"> 
 <tbody> 
  <tr> 
   <td> <b> Parameters:</b> </td> 
   <td> <p> 
     <ul id="ul_632C900B09514E1DBAFD978918C349E3"> 
      <li id="li_FBEE8389D0AB42909BF085B4C6903B92"><span class="codeph">name(<span class="varname"> str</span>)</span> <p> Name of the object. </p> </li> 
      <li id="li_047F43CA52C44C87A0F19853F3BDF45E"><span class="codeph">mask(<a href="../../../c-s7vampy-api-reference/c-classes/c-classes-image/r-class-s7vampy.image.image.md#reference-9f763e9b74dc47549877ee15bd0cdb94" format="dita" scope="local"> s7vampy.image.Image</a>)</span> <p>Mask of the object. </p> </li> 
      <li id="li_94C10F9A754F47FDA90173376983A44C"><span class="codeph">overlap(<span class="varname"> bool</span>)</span> <p> Defaults to false. <span class="codeph"> Overlap</span> is a keyword argument and needs to be specified explicitly. <span class="codeph"> Specifyoverlap=True</span> to create an overlap object. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> Returns:</b> </td> 
   <td> <p><span class="codeph"><a href="../../../c-s7vampy-api-reference/c-classes/c-objects/r-class-s7vampy-obj-flatobject.md#reference-e6da5ec8f3564cd088891e6c64205552" format="dita" scope="local"> FlatObject</a></span> </p> <p> New object. </p> </td> 
  </tr> 
 </tbody> 
</table>

Add a flat texturable object to this group.

The provided mask must be the same size as the vignette view.

`add_group (name)`

<table id="table_D868CD4A77D84F15BB3573085591E02A"> 
 <tbody> 
  <tr> 
   <td> <b> Parameters:</b> </td> 
   <td> <p> <span class="codeph">name (<span class="varname"> str</span>)</span> </p> <p> Name of the new object group. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> Returns:</b> </td> 
   <td> <p><span class="codeph"><a href="../../../c-s7vampy-api-reference/c-classes/c-objects/r-class-s7vampy-obj-group.md#reference-d4268759bb7740659019fec3eb7cbe91" format="dita" scope="local"> Group</a></span> </p> <p> New object group. </p> </td> 
  </tr> 
 </tbody> 
</table>

Add an object group to this group.

` add_nontexturable_object ( *`name`*, *`mask`*, *`*_`*, *`**keywords`*)`

<table id="table_82D12D0CFC554D9C90BDA549B53EDB39"> 
 <tbody> 
  <tr> 
   <td> <b> Parameters:</b> </td> 
   <td> <p> 
     <ul id="ul_CF2D342D36E1415AA4AFB0088E8305E2"> 
      <li id="li_FEBADF07523D4A4A9A909B71DD02E53B"><span class="codeph">name(<span class="varname"> str</span>)</span> <p>Name of the object. </p> </li> 
      <li id="li_A559157F77FE42CE81912D25E703ED4A"><span class="codeph">mask(<a href="../../../c-s7vampy-api-reference/c-classes/c-classes-image/r-class-s7vampy.image.image.md#reference-9f763e9b74dc47549877ee15bd0cdb94" format="dita" scope="local"> s7vampy.image.Image</a>)</span> <p>Mask image associated with the object. </p> </li> 
      <li id="li_76F9C1F39A9E4C7BBC7C82CF587B8C44"><span class="codeph">overlap(<span class="varname"> bool</span>) </span> <p>Defaults to false. <span class="codeph"> Overlap</span> is a keyword argument and needs to be specified explicitly. Specify <span class="codeph"> overlap=True</span> to create an overlap object. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> Returns:</b> </td> 
   <td> <p><span class="codeph"><a href="../../../c-s7vampy-api-reference/c-classes/c-objects/r-class-s7vampy-obj-nontexturableobject.md#reference-161cbb70e49e47ed908036ec35db68cc" format="dita" scope="local"> NonTexturableObject</a></span> </p> <p> New object. </p> </td> 
  </tr> 
 </tbody> 
</table>

Add a non-texturable object to this group.

The provided mask must be the same size as the vignette view.

`add_static_object ( *`name`*, *`mask`*)`

<table id="table_9141A18DE967461581D0308B73A789CF"> 
 <tbody> 
  <tr> 
   <td> <b> Parameters:</b> </td> 
   <td> <p> 
     <ul id="ul_DC18E766F98A485090DCEBA0589AE4C3"> 
      <li id="li_2ADDA3D196544A29A54A99CF9AE4D136"><span class="codeph">name(<span class="varname"> str</span>)</span> <p>Name of the object. </p> </li> 
      <li id="li_04D1E887F3E94F08BDAA9D717B55D0CA"><span class="codeph">mask(<a href="../../../c-s7vampy-api-reference/c-classes/c-classes-image/r-class-s7vampy.image.image.md#reference-9f763e9b74dc47549877ee15bd0cdb94" format="dita" scope="local"> s7vampy.image.Image</a>)</span> <p>Mask image associated with the object. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> Returns:</b> </td> 
   <td> <p><span class="codeph"><a href="../../../c-s7vampy-api-reference/c-classes/c-objects/r-class-s7vampy-obj-staticobject.md#reference-bd09110f7ce04b6d88fdf1c5f1a72804" format="dita" scope="local"> StaticObject</a></span> </p> <p> New object. </p> </td> 
  </tr> 
 </tbody> 
</table>

Add a static object to this group.

The provided mask must be the same size as the vignette view.

` add_static_overlap_object ( *`name`*, *`image`*)`

<table id="table_D77BC93CB03E436BA1652F792563D45D"> 
 <tbody> 
  <tr> 
   <td> <b> Parameters:</b> </td> 
   <td> <p> 
     <ul id="ul_74D2CF45A24840D1A187E7DB4720A8CD"> 
      <li id="li_318792651DE64301878863DE38BF4B71"><span class="codeph">name(<span class="varname"> str</span>)</span> <p>Name of the object. </p> </li> 
      <li id="li_BAB64DD736874621984EA76FBEC4A4D3"><span class="codeph">image(<a href="../../../c-s7vampy-api-reference/c-classes/c-classes-image/r-class-s7vampy.image.image.md#reference-9f763e9b74dc47549877ee15bd0cdb94" format="dita" scope="local"> s7vampy.image.Image</a>)</span> <p>Static overlap image (must be RGBA). </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> Returns:</b> </td> 
   <td> <p><span class="codeph"><a href="../../../c-s7vampy-api-reference/c-classes/c-objects/r-class-s7vampy-obj-staticoverlapobject.md#reference-7b66780df1fc40cfa436fecdc16037c5" format="dita" scope="local"> StaticOverlapObject </a></span> </p> <p> New object. </p> </td> 
  </tr> 
 </tbody> 
</table>

Add a static overlap object to this group.

The provided static overlap image must be the same size as the vignette view.

` add_surface_object ( *`name`*, *`mask`*, *`*_`*, *`**keywords`*)`

<table id="table_E57BB108E8CD47FA99F04782C83A5838"> 
 <tbody> 
  <tr> 
   <td> <b> Parameters:</b> </td> 
   <td> <p> 
     <ul id="ul_FFEAE44B2A7C470C80FC8353EC55FE70"> 
      <li id="li_2675DD4CF925433AB8EC7BF15A6847D9"><span class="codeph">name(<span class="varname"> str</span>)</span> <p>Name of the object. </p> </li> 
      <li id="li_B53F59A27DDB4484AE20BDCCE9CEFFD6">mask(<span class="codeph"><a href="../../../c-s7vampy-api-reference/c-classes/c-classes-image/r-class-s7vampy.image.image.md#reference-9f763e9b74dc47549877ee15bd0cdb94" format="dita" scope="local"> s7vampy.image.Image</a></span>) - Mask of the object. </li> 
      <li id="li_88DF48E0B89A43178AB8F11570B5AB5C"><span class="codeph">overlap(<span class="varname"> bool</span>)</span> <p>Defaults to false. <span class="codeph"> Overlap</span> is a keyword argument and needs to be specified explicitly. Specify <span class="codeph"> overlap=True</span> to create an overlap object. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> Returns:</b> </td> 
   <td> <p><span class="codeph"><a href="../../../c-s7vampy-api-reference/c-classes/c-objects/r-class-s7vampy-obj-surfaceobject.md#reference-cf2b73b972e84cf5b9a0e22ab3d106f4" format="dita" scope="local"> SurfaceObject</a></span> </p> <p> New object. </p> </td> 
  </tr> 
 </tbody> 
</table>

Add a surface texturable (flowline) object to this group.

The provided mask must be the same size as the vignette view.

`children [ObjectList]`

List of objects and object groups that are children of this object group ( ` [ObjectList](../../../c-s7vampy-api-reference/c-classes/c-objects/r-class-s7vampy-obj-objectlist.md#reference-0b83540fd1e9495c8d00f19bfb27656b)`).

`imagemap [s7vampy.path.Path]`

Image map associated with the object group ( ` [s7vampy.path.Path](../../../c-s7vampy-api-reference/c-classes/c-path/r-class-s7vampy-path-path.md#reference-2e340c8f51db4053877c584873a41bea)`). 
