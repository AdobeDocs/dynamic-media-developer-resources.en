---
description: Objects and object groups are stored in a hierarchy.
seo-description: Objects and object groups are stored in a hierarchy.
seo-title: class s7vampy.obj.ObjectHierarchy(vignette)
title: class s7vampy.obj.ObjectHierarchy(vignette)
uuid: 2c56563c-8830-4f5e-9424-03fe70fd0e8a
index: y
internal: n
snippet: y
---

# class s7vampy.obj.ObjectHierarchy(vignette){#class-s-vampy-obj-objecthierarchy-vignette}

Objects and object groups are stored in a hierarchy.

 At the top of the hierarchy there is a background object that contains the background mask, and a set of zero or more object groups. Each object group may contain one or more objects and object groups.

Access the object hierarchy stored in a vignette using the ` [s7vampy.vignette.Vignette.objects](../../../c-s7vampy-api-reference/c-classes/c-vignette/r-class-s7vampy-vignette-vignette.md#reference-b63a48cb2bd04a1d98930e059a0f3678)` attribute. The returned `ObjectHierarchy` instance can be used to add more objects and object groups or change attributes of existing objects and object groups.

The `ObjectHierarchy` class provides the following capabilities:

* len(hierarchy) returns the number of objects and object groups in the hierarchy. 
* A depth first iterator iterates over all objects and object groups. 
* An index operator makes it easy to find an object in the hierarchy. For example hierarchy["group/obj1"] returns an instance of 'obj1' in the group named 'group'. 
* The in operator can be used to check for the existence of objects and object groups. For example, "group/obj1" in hierarchy returns True if an object named 'obj1' exists in group 'group'.

Consider the following hierarchy:

* grp1

    * obj1 
    * obj2

* grp2

    * obj1 
    * obj2

**Create the hierarchy in a new vignette: **

```
>>> from s7vampy import *
>>> v = create_vignette(open_image("TestData/view.png"))
>>> grp1 = v.objects.add_group("grp1")
>>> grp1.add_nontexturable_object("obj1", open_image("TestData/obj11-mask.png"))
>>> grp1.add_nontexturable_object("obj2", open_image("TestData/obj12-mask.png"))
>>> grp2 = v.objects.add_group("grp2")
>>> grp2.add_nontexturable_object("obj1", open_image("TestData/obj21-mask.png"))
>>> grp2.add_nontexturable_object("obj2", open_image("TestData/obj22-mask.png"))
```

**Use the index operator to find objects and groups by name:**

```
>>> v.objects["grp1/obj1"]
>>> v.objects["grp2"]
```

**Use the in operator to check for the existence of an object:**

```
>>> if "grp1/obj1" in v.objects:
...      print "Found grp1/obj1"
Found grp1/obj1
```

**Both the index and in operator are case-insensitive:**

```
>>> if "GRP1/OBJ1" in v.objects:
...      print hierarchy["GRP1/OBJ1"]
```

**Use the iterator to iterate over all groups and objects:**

```
>>> for o in v.objects:
...     print o.path
grp1
grp1/obj1
grp1/obj2
grp2
grp2/obj1
grp2/obj2
```

**Use ` *`len()`*` to find the total number of groups and objects: **

```
>>> len(v.objects)
6
```

`add_group ( name )`

<table id="table_AA9E7D78F7254D748842C1A05AD9A7AF"> 
 <tbody> 
  <tr> 
   <td> <b> Parameters:</b> </td> 
   <td> <p> <span class="codeph"> name (str)</span> </p> <p>Name of the new object group. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> Returns:</b> </td> 
   <td> <p><span class="codeph"> Group</span> </p> <p> New object group. </p> </td> 
  </tr> 
 </tbody> 
</table>

Add an object group to the top of the object hierarchy.

`children`

List that contains the background object and the top-level object groups ( ` [ObjectList](../../../c-s7vampy-api-reference/c-classes/c-objects/r-class-s7vampy-obj-objectlist.md#reference-0b83540fd1e9495c8d00f19bfb27656b)`). 
