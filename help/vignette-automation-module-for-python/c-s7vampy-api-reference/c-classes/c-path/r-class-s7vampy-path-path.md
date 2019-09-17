---
description: Paths are built from a set of independent contours. Each contour contains a series of connected line segments.
seo-description: Paths are built from a set of independent contours. Each contour contains a series of connected line segments.
seo-title: class s7vampy.path.Path
title: class s7vampy.path.Path
uuid: 233c5d1d-cb57-4db9-a2a9-26b86118832d
---

# class s7vampy.path.Path{#class-s-vampy-path-path}

Paths are built from a set of independent contours. Each contour contains a series of connected line segments.

 `add_contour ( *`points`*)`

<table id="table_20085D456C1645E19A49FFB2557E4F10"> 
 <tbody> 
  <tr> 
   <td> <b> Parameters:</b> </td> 
   <td> <p> <span class="codeph">points (<span class="varname"> list</span>)</span> </p> <p>List of (x, y) tuples. Must contain at least two points. </p> </td> 
  </tr> 
 </tbody> 
</table>

Add a contour defined as a list of points to the path.

`close ()`

Close the last contour of the path. Does nothing if the contour is already closed.

`close_all ()`

Close all contours. Does nothing to contours that are already closed.

`contours`

Iterator that runs over the contours.

`empty [bool, read-only]`

Check if the path is empty.

`lineto ( *`x`*, *`y`*)`

<table id="table_F66D6BF6D6074CA381461153EACF127C"> 
 <tbody> 
  <tr> 
   <td> <b> Parameters:</b> </td> 
   <td> <p> 
     <ul id="ul_D8D18DB9B4B34F318A400E4D26DFC508"> 
      <li id="li_9CEAB80696BE42278586234BFE16521D"><span class="codeph"> x</span> <p>Point x-value </p> </li> 
      <li id="li_9BEE1C12D56D4B44818F41162FBAB4D6"><span class="codeph"> y</span> <p>Point y-value </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Create a new line segment starting at the last added point and ending at the given coordinate.

` moveto ( *`x`*, *`y`*)`

<table id="table_80EB2E4AF6084F4A87AEEE32EF8C1D8E"> 
 <tbody> 
  <tr> 
   <td> <b> Parameters:</b> </td> 
   <td> <p> 
     <ul id="ul_096712331E4B4630A160E61D58163B30"> 
      <li id="li_FA44CAE6E50D4D7E87CF071CC4B4FA00"><span class="codeph"> x</span> <p>Point x-value </p> </li> 
      <li id="li_3C8EEFAB95C24BD1A69BC324B7B67011"><span class="codeph"> y</span> <p>Point y-value </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Create a new contour starting at the given point.

`num_contours [int, read-only]`

Return the total number of contours.

`num_segments [int, read-only]`

Return the total number of segments.

` rlineto ( *`x`*, *`y`*)`

<table id="table_C3F6333B0FB6480C84DDF3E4B64C3FE4"> 
 <tbody> 
  <tr> 
   <td> <b> Parameters:</b> </td> 
   <td> <p> 
     <ul id="ul_017645BA9F9E42D4BDAAEAE29B23EF9B"> 
      <li id="li_3B3B4F209E1E4A2B960144B70E34D57D"><span class="codeph"> x</span> <p>Point x-value </p> </li> 
      <li id="li_AEC8535022544B1388253D7E2048F0E7"><span class="codeph"> y</span> <p>Point y-value </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Create a new line segment starting at the last added point and ending at the given coordinate. The point is relative to the last point added to the path.

` rmoveto ( *`x`*, *`y`*)`

<table id="table_7411C969951643A38DADFA514DB1C8D9"> 
 <tbody> 
  <tr> 
   <td> <b> Parameters:</b> </td> 
   <td> <p> 
     <ul id="ul_C300EF6F104845189C0EBF46F28911C4"> 
      <li id="li_2D1DE3DB80BC4D71A347356856947B82"><span class="codeph"> x</span> <p>Point x-value </p> </li> 
      <li id="li_1470C732F91347D7AC21CF2F6751DC05"><span class="codeph"> y</span> <p>Point y-value </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Create a new contour starting at the given point. The point is relative to the last point added to the path.

`segments`

Generator that returns all segments. 
