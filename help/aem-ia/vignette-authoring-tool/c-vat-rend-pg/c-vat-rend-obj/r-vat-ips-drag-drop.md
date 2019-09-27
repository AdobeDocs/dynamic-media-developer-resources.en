---
description: If you plan to drag and drop images from IPS into Image Authoring for rendering, be aware that certain values from IPS are used during rendering.
seo-description: If you plan to drag and drop images from IPS into Image Authoring for rendering, be aware that certain values from IPS are used during rendering.
seo-title: Setting Up IPS for Dragging and Dropping
solution: Experience Manager
title: Setting Up IPS for Dragging and Dropping
topic: Scene7 Image Authoring
uuid: 15eefbef-ec30-40a4-8ca2-d76fc9be8e6d
---

# Setting Up IPS for Dragging and Dropping{#setting-up-ips-for-dragging-and-dropping}

If you plan to drag and drop images from IPS into Image Authoring for rendering, be aware that certain values from IPS are used during rendering.

## Resolution {#resolution}

The resolution and anchor points set for images in IPS are used by [!DNL Image Authoring]. If the resolution for an image in IPS is set to zero, [!DNL Image Authoring] uses the default value set in the IPS [!DNL Image Rendering Publish Settings]. If that value is also zero, [!DNL Image Authoring] uses its own default, set in the [ [!DNL Material Properties] dialog box](../../c-vat-rend-pg/c-vat-work-text/c-vat-text-mat-prop/c-vat-text-mat-prop.md#concept-56e919cfd48748169dc2f011aa95c5fd).

## User-defined Fields {#user-defined-fields}

You may need to set up certain user-defined fields in IPS. These fields are not required, unless you are applying decals or borders from IPS, in which case the [!DNL Repeat] field is required. However, if you set up the fields and use drag-and-drop from IPS, the field values are used by [!DNL Image Authoring]. The fields to set up are as follows: 

<table id="table_CDE24476FD75423ABE030682729737E2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> User-defined field </th> 
   <th colname="col2" class="entry"> Definition </th> 
   <th colname="col3" class="entry"> Recommended Values </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Color </td> 
   <td colname="col2"> Used to colorize textures. Specify a hexadecimal value where the first number is Red, the second number is Blue, and the third number is Green. </td> 
   <td colname="col3"> #00aabb or 0x00aabb </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Type </td> 
   <td colname="col2"> Determines the material type. </td> 
   <td colname="col3"> 0 to 19 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gloss </td> 
   <td colname="col2">Determines which <span class="wintitle"> Illumination Map</span> is used. </td> 
   <td colname="col3"> -1 to 100, inclusive -1=default </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Roughness </td> 
   <td colname="col2"> Determines the roughness of the material type. </td> 
   <td colname="col3"> -1 to 100, inclusive -1=default value </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sharp </td> 
   <td colname="col2"> Sharpens the material image. </td> 
   <td colname="col3"> 0-2 (0=none, 1=normal, 2=more) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Repeat </td> 
   <td colname="col2"> <p>0 straight </p> <p>1 4-way random tiling </p> <p>2 8-way random tiling </p> <p>3 diamond tiling </p> <p>4 book-match (mirror) </p> <p>5 half-across </p> <p>6 half-drop wallpaper hang </p> <p>7 fifth-drop wallpaper hang </p> <p>8 reverse wallpaper hang </p> <p>9 random wallpaper hang </p> <p>10 random drop </p> <p>11 random across </p> <p>12 horizontal repeat only (wall border) </p> <p>13 vertical repeat only (reserved for future) </p> <p>14 not repeated (decal) </p> </td> 
   <td colname="col3"> 14 (decals) or 12 (borders) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> BaseColor </td> 
   <td colname="col2"> Determines the background color of the material. </td> 
   <td colname="col3"> #00aabb or 0x00aabb </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Alignment </td> 
   <td colname="col2"> Determines the origin of the material. </td> 
   <td colname="col3">0-6 (0=center, 1=continuous, 2=random, 3-6 whatever is added to <span class="filepath"> vat.ini</span>) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Illum </td> 
   <td colname="col2">Determines which <span class="wintitle"> Illumination Map</span> a material uses for rendering. </td> 
   <td colname="col3"> -1-2 (-1=Auto-Detect, 0=Map A, 1=Map B, 2=Map C) </td> 
  </tr> 
 </tbody> 
</table>

The field names are not case-sensitive, but they must be spelled exactly as shown here. Do not add spaces, underscores, or other characters.

To create user-defined fields in IPS, you must have Company or IPS Administrator rights. Consult the Administrator section of the IPS Help for instructions on creating user-defined fields. 