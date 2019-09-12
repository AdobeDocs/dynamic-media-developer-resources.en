---
description: The ObjectList contains a list of objects and groups that are all at the same level of the hierarchy.
seo-description: The ObjectList contains a list of objects and groups that are all at the same level of the hierarchy.
seo-title: class s7vampy.obj.ObjectList(factory, parent, object_list)
title: class s7vampy.obj.ObjectList(factory, parent, object_list)
uuid: 8e7763cc-1206-48d8-baf7-9e0d64728193
index: y
internal: n
snippet: y
---

# class s7vampy.obj.ObjectList(factory, parent, object_list){#class-s-vampy-obj-objectlist-factory-parent-object-list}

The ObjectList contains a list of objects and groups that are all at the same level of the hierarchy.

 All objects and groups in the `ObjectList` are derived from the class ` [Object](../../../c-s7vampy-api-reference/c-classes/c-objects/c-objects.md#concept-a4eae8224c374af2b60aa54fd163e7ae)`.

Objects and groups added to the list can be indexed and found by name and by index.

The `ObjectList` class provides the following capabilities:

* len(object_list) returns the number of objects and groups. 
* Iterate and reverse iterate over the objects and groups. 
* Look-up objects using the index operator by name or by numeric index. Name lookup is case-insensitive. 
* Check for existence of object and groups by name. Name lookup is case-insensitive.

Consider the following list:

* group1 
* group2 
* object1 
* object2

You can use the *`index`* operator to find objects by name:

```
>>> object1 = object_list["object1"]
```

The *`index`* operator is case-insensitive, so this also works:

```
>>> object1 = object_list["OBJECT1"]
```

The index operator can also be used to index by number:

```
>>> object1 = object_list[2]
```

You can use the *`in`* operator to check for the existence of objects or groups by name:

```
>>> if "object1" in object_list: 
...     print "Found object1!" 
Found object1! 
>>> if "OBJECT2" in object_list: 
...     print "Found object2!" 
Found object2!
```

You can use the iterator to iterate over the objects and groups in the list:

```
>>> for obj in object_list: 
...     print obj.name 
group1 
group2 
object1 
object2
```

You can use the *`reversed()`* function to reverse the iterator:

```
>>> for obj in reversed (object_list): 
...     print obj.name 
object2 
object1 
group2 
group1
```

You can use *`len()`* to find the total number of items in the list:

```
>>> len(object_list) 
4
```

`ObjectList` instances are returned from the ` [ObjectHierarchy.children](../../../c-s7vampy-api-reference/c-classes/c-objects/r-s7vampy-obj-objecthierarchy.md#reference-de34c2cc4dbf49e1878b190fffa646bb)` and ` [Group.children](../../../c-s7vampy-api-reference/c-classes/c-objects/r-class-s7vampy-obj-group.md#reference-d4268759bb7740659019fec3eb7cbe91)` properties.

`count (name)`

<table id="table_35839B41BDC04D9788A798D5A8DC2BBF"> 
 <tbody> 
  <tr> 
   <td> <b> Parameters:</b> </td> 
   <td> <p> <span class="codeph"> name (str) </span> </p> <p>Name of the object or group to search for. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> Returns:</b> </td> 
   <td> <p> Number of objects or groups with the given name. </p> </td> 
  </tr> 
 </tbody> 
</table>

Return the number of objects or groups with the given name. The search is case-insensitive.

`index (name)`

<table id="table_21FAE5A1D9F0448795C38A06028D3584"> 
 <tbody> 
  <tr> 
   <td> <b> Parameters:</b> </td> 
   <td> <p> <span class="codeph"> name (str) </span> </p> <p>Name of the object or group to search for. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> Returns:</b> </td> 
   <td> <p> Index of the object or group. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> Raises :</b> </td> 
   <td> <p> <span class="codeph"> ValueError </span> if the object or group can't be found. </p> </td> 
  </tr> 
 </tbody> 
</table>

Find the first object or group with the given name. The search is case-insensitive. 
