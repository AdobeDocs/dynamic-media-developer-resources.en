---
title: FXG server protocol
description: To manipulate a graphic, you can use reference points similar to compass points.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 57d9ba37-819e-455f-9b22-bd7aabffe007
TQID: https://experienceleague.adobe.com/6kxGdecj7xO4J6sxBWtd4esIt-ykc1gpRhJIaoYKZ-8
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# FXG server protocol{#fxg-server-protocol}

To manipulate a graphic, you can use reference points similar to compass points.

Using reference points, you can rotate, scale, or resize a graphic relative to a particular reference point. The reference points are `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`, `south`, and `southeast`. For example, by using the center reference point, you can rotate a graphic by 45° on its center. The following image shows where the reference points are located, a graphic, the graphic rotated 20° from its `northWest` reference point, and the graphic rotated 20° from its `east` reference point.

![Reference points image](assets/wp_ref_points.png)

* A. Reference point locations
* B. A graphic
* C. The graphic rotated 20° from its `northWest` reference point
* D. The graphic rotated 20° from its `east` reference point

The syntax is:

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

The default value is none. The `inherit` value passes the `s7:referencePoint` value, provided it is not `none`, from the top of the page or group level to all children. The `none` setting means that there is no reference point for the object and the FXG coordinate system is used.

>[!NOTE]
>
>To use a reference point and not have any displacement in the object after it is manipulated, update the x and y values of the object after you manipulate it.

When a value from `s7:referencePoint` is used with groups (or paths, line elements, or any element that doesn’t have explicit width and height definitions), the value applies to the cumulative bounding box of the group. For example, the top-left point of the bounding box of all the objects in the group serves as the `northWest` reference point for the group; the bottom-right point serves as the `southEast` reference point.
