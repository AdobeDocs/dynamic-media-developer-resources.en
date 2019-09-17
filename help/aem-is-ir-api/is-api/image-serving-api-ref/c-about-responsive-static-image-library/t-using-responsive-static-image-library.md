---
description: To add Responsive Image library to a web page and manage existing images with the library, complete the following steps.
seo-description: To add Responsive Image library to a web page and manage existing images with the library, complete the following steps.
seo-title: Using Responsive Image library
solution: Experience Manager
title: Using Responsive Image library
topic: Scene7 Image Serving - Image Rendering API
uuid: 325cdc8d-2bfa-4f9b-bf88-51d1dcc6c495
---

# Using Responsive Image library{#using-responsive-image-library}

To add Responsive Image library to a web page and manage existing images with the library, complete the following steps.

**To use Responsive Image library** 

1. In SPS, [create an Image Preset](http://help.adobe.com/en_US/scene7/using/WS2F6A1049-B41F-447d-A520-91227F9CDABF.html) in case you plan to use Responsive Image library with presets.

   When you define Image Presets that are used with Responsive Image Library, do not use any settings that affect image size, such as `wid=`, `hei=`, or `scl=`. Do not specify any size fields in the Image Preset. Instead, leave them as blank values. 
1. Add the library JavaScript file to your web page.

   Before you can use library API, be sure that you include `responsive_image.js`. This JavaScript file is located in the `libs/` subfolder of your standard IS-Viewers deployment:

   `<s7viewers_root>/libs/responsive_image.js` 
1. Set up existing images.

   The library reads certain configuration attributes from an image instance it is working with. Define attributes before the `s7responsiveImage` API function is called for such image.

   It is also suggested that you put the existing image URL into the `data-src` attribute. Then, set up the existing `src` attribute to have a 1x1 GIF image encoded as Data URI. Doing so, reduces the number of HTTP requests that are sent by the web page at load time. Note, however, that if SEO (search engine optimization) is needed, it is better to set up a `title` attribute on the image instance.

   The following is an example of defining `data-breakpoints` attribute for the image and using a 1x1 GIF encoded as Data URI:

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. Call the `s7responsiveImage` API function for every image instance that the library manages.

   Call the `s7responsiveImage` API function for every image instance that the library manages. After such a call, the library replaces the original image with the image that is downloaded from Image Serving according to the runtime size of the `IMG` element in the web page layout and the device screen's density.

   The following code is an example of calling `s7responsiveImage` API function on an image, assuming that `responsiveImage` is an ID of that image:

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## Example {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

The library supports working with many image instances on the web page simultaneously. Therefore, repeat steps 1 and 2 above for each image that you want the library to manage.

It is the responsibility of the web page to style the image element to make it flexible in size. The Responsive Image library itself does not differentiate between fixed-size and "fluid" images. If applied to a fixed-size image it loads the new image only once.

The following code is a complete example of a trivial web page that has a single fluid image managed by the Responsive Image library. The example contains extra CSS styling to make the image "responsive" to the web browser window size:

```
<!DOCTYPE html> 
<html> 
 <head> 
  <style type="text/css"> 
  .container { 
   width: 50%; 
  } 
  .fluidimage { 
   max-width: 100%; 
  } 
  </style> 
 </head> 
 <body> 
  <div class="container"> 
   <img id="responsiveImage" src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="200,400,600,800" class="fluidimage"> 
  </div> 
  <script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/libs/responsive_image.js"></script> 
  <script type="text/javascript"> 
   s7responsiveImage(document.getElementById("responsiveImage")); 
  </script> 
 </body> 
</html>
```

**Using Smart Crop**

There are two Smart Crop modes available in AEM 6.4 and Scene7 Viewers 5.9:

* **Manual** - user-defined breakpoints and corresponding Image Service commands are defined within an attribute in the image element. 
* **Smart Crop** - computed smart crop renditions are automatically retrieved from the delivery server. The best rendition is selected using the runtime size of the image element.

To use Smart Crop mode you set the `data-mode` attribute to `smart crop`. For example:

```
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

The associated image element dispatches a `s7responsiveViewer` event during runtime when the breakpoint changes.

```
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
