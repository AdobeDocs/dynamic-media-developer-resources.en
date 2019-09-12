---
description: Contours contain a series of connected line segments.
seo-description: Contours contain a series of connected line segments.
seo-title: class s7vampy.path.Contour
title: class s7vampy.path.Contour
uuid: d8921a58-1b8b-438d-a5cf-cb258943dd85
index: y
internal: n
snippet: y
---

# class s7vampy.path.Contour{#class-s-vampy-path-contour}

Contours contain a series of connected line segments.

A contour can be closed (where the last point equals the first point), or remain open.

Contours are continuous, meaning that there are no gaps from one segment to another.

Contours should never be created directly. Instead, use the [Path](../../../c-s7vampy-api-reference/c-classes/c-path/r-class-s7vampy-path-path.md#reference-2e340c8f51db4053877c584873a41bea) class to build them. Contours are typically modified using the [Path](../../../c-s7vampy-api-reference/c-classes/c-path/r-class-s7vampy-path-path.md#reference-2e340c8f51db4053877c584873a41bea) class.

The Contour class provides the following capabilities:

* `len(contour)` that returns the number of segments. 
* An iterator that iterates over the segments. 
* An index operator that finds a line segment by index.

` append ( *`segment`*)`

<table id="table_221FFBD58B284FFF9D85F66928AC69D3"> 
 <tbody> 
  <tr> 
   <td> <b> Parameters:</b> </td> 
   <td> <p><span class="codeph"> segment (<a href="../../../c-s7vampy-api-reference/c-classes/c-path/r-class-s7vampy-path-segment.md#reference-d75a42c8e22b4d1dbddbb8d72109e7bb" format="dita" scope="local"><span class="varname"> Segment</span></a>)</span> </p> <p>Segment instance. </p> </td> 
  </tr> 
 </tbody> 
</table>

Append a segment to the list.

`close ()`

Close the contour.

`closed [bool, read-only]`

Check if the contour is closed. 
