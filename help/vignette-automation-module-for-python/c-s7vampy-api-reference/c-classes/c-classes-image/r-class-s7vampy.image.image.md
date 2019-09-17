---
description: Represents an image that is loaded into memory.
seo-description: Represents an image that is loaded into memory.
seo-title: class s7vampy.image.Image(image)
title: class s7vampy.image.Image(image)
uuid: 51764f21-f53b-4ae0-aa21-8b3ba9ff056b
---

# class s7vampy.image.Image(image){#class-s-vampy-image-image-image}

Represents an image that is loaded into memory.

Images are immutable. All Image methods and properties either return information about the image or return a new image instance.

Images are either loaded into memory using the ` [s7vampy.open_image()](../../../c-s7vampy-api-reference/c-functions/r-s7vampy.open-image.md#reference-2b48fba87ed74447b8590ff162c49c17)` function or when an image is referenced that is stored in a vignette.

`has_alpha [bool, read-only]`

Presence of an alpha channel.

`name [str, read-only]`

Name of the image.

**`save(filename, fmt)`**

<table id="table_2D9CA396EE43499E87671F82F7BFD63D"> 
 <tbody> 
  <tr> 
   <td> <b> Parameters:</b> </td> 
   <td> <p> 
     <ul id="ul_BC5B6B92CE9E44638ABC5F46C964D703"> 
      <li id="li_9F1156B311184C11A3893734AB4279B3"><span class="codeph"> filename(str)</span> <p>Name of the exported file. </p> </li> 
      <li id="li_772BA7AFA2D34947850AEE1101DF019C"><span class="codeph"> fmt(str)</span> <p>Image file format ('<span class="codeph"> BMP</span>', '<span class="codeph"> JPEG</span>', '<span class="codeph"> PNG</span>', or '<span class="codeph"> TIFF</span>') </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Save image to disk.

Export images stored in a vignette to disk. Currently the BMP, JPEG, PNG, and TIFF file formats are supported. The format string is not case sensitive.

`size [tuple, read-only]`

Size in pixels (width, height). 
