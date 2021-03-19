---
description: Configuration attributes are defined as attributes directly on an IMG element that the Responsive Image library manages. Each image can have its own set of attributes.
seo-description: Configuration attributes are defined as attributes directly on an IMG element that the Responsive Image library manages. Each image can have its own set of attributes.
seo-title: Command reference – Configuration attributes
solution: Experience Manager
title: Command reference – Configuration attributes
uuid: a3d52680-2a28-40c8-9b5f-b1c252c88e4d
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Business Practitioner"
---

# Command reference – Configuration attributes{#command-reference-configuration-attributes}

Configuration attributes are defined as attributes directly on an IMG element that the Responsive Image library manages. Each image can have its own set of attributes.

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

Optional.

URL to the image that Image Serving serves up. If the URL is not present, the library uses the value that is set in `src` attribute as fall back. This attribute serves the initial image and the dynamic image that the Responsive Image library manages from different locations.

**Example** 

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

If `data-src` is set, `src` is optional, and can contain any URL that you want to add. For example, it can contain a URL to the same Image Serving-based image that the library uses. Or, it can contain a GIF placeholder, or even a data URI to avoid an extra server round trip on startup.

If `data-src` is not set, `src` is mandatory and must contain a URL to the image that Image Serving serves up.

**Example**

Using data URI for the `src` attribute and Image Serving URL for the `data-src` attribute:

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## data-breakpoints {#section-3bf62a89ff3e40569848c1fe3ac7886c}

A comma-separated list of breakpoints and optionally followed with a colon ( `:`), and Image Serving commands or Image Presets. Each breakpoint is an image width value defined in logical CSS pixels. The library loads the image with the closest larger value from the list and downscale it on the client to match the runtime CSS image width. (If you work on a high-density screen, image renditions that are loaded from the server represent breakpoint values multiplied by the device's pixel ratio).

For any breakpoint from the list, it is possible to define one or more Image Serving commands or Image Preset names. Such extra parameters are only applied to the image in case this particular breakpoint is currently active.

You can use any supported Image Serving command except for those view commands that affect response image size, like `wid=`, `hei=`, or `scl=`. The same restriction applies to Image Presets: an Image Preset used with Responsive Image Library must not contain such commands.

Multiple Image Serving commands or Image Preset names are separated with " `&`" character. If an Image Serving command has a comma in its value, such comma is replaced with `%2C`. Image Preset names are wrapped in dollar signs ( `$`).

**Examples**

**Using breakpoints only**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**Using Image Serving commands**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**Using Image Presets**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**Using Image Presets & Image Serving commands**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`

## data-mode {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

The following two Smart Crop modes are available in AEM 6.4 and higher and Dynamic Media Viewers 5.9 and higher:

* **Manual** - user-defined breakpoints and corresponding Image Service commands are defined within an attribute in the image element. 
* **Smart Crop** - computed smart crop renditions are automatically retrieved from the delivery server. The best rendition is selected using the runtime size of the image element.

To use Smart Crop mode you set the `data-mode` attribute to `smart crop`.

**Example** 

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

