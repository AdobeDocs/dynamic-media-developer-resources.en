---
description: Create a new path.
seo-description: Create a new path.
seo-title: s7vampy.create_path()
title: s7vampy.create_path()
uuid: 0b255cc1-58f5-422f-b80d-e575e7d3d441
index: y
internal: n
snippet: y
---

# s7vampy.create_path(){#s-vampy-create-path}

Create a new path.

<table id="table_D41317F7E3D1416B8069C10D66CBB6B6"> 
 <tbody> 
  <tr> 
   <td> <b> Returns:</b> </td> 
   <td> <p> <span class="codeph"> Path</span> </p> <p>Empty path instance </p> </td> 
  </tr> 
 </tbody> 
</table>

**Build a path containing an unclosed triangle and a rectangle contour:**

```
>>> from s7vampy import *
>>> p = create_path ()
>>> p.moveto(0, 100)
>>> p.rlineto(50, -100)
>>> p.rlineto(50, 100)
>>> p.moveto(200, 0)
>>> p.rlineto(100, 0)
>>> p.rlineto(0, 100)
>>> p.rlineto(-100, 0)
>>> p.close()
```

**Iterate over the path:**

```
>>> for c in p.contours:
>>>     print "Num segments:", len(c)
>>>     # Iterate over the segments in the contour
>>>     for seg in c:
>>>          print seg
Num segments: 2
[(0, 100), (50, 0)]
[(50, 0), (100, 100)]
Num segments: 4
[(200, 0), (300, 0)]
[(300, 0), (300, 100)]
[(300, 100), (200, 100)]
[(200, 100), (200, 0)]
```

