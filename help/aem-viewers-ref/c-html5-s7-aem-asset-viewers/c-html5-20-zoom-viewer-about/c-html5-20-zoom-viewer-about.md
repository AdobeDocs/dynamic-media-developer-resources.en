---
title: Zoom
description: Zoom Viewer is an image viewer that displays a zoomable image. This viewer works with image sets and navigation is done by using swatches. It has zoom tools, full-screen support, swatches, and an optional close button. It is designed to work on desktops and mobile devices.
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 81a74026-fb15-4f57-a4c7-1ab005950245
---
# Zoom{#zoom}

Zoom Viewer is an image viewer that displays a zoomable image. This viewer works with image sets and navigation is done by using swatches. It has zoom tools, full-screen support, swatches, and an optional close button. It is designed to work on desktops and mobile devices.

>[!NOTE]
>
>Images which use IR (Image Rendering) or UGC (User-Generated Content) are not supported by this viewer.

Viewer type 502.

See [System requirements and prerequisites](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Demo URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## Using Zoom Viewer {#section-e6c68406ecdc4de781df182bbd8088b4}

Zoom Viewer represents a main JavaScript file and a set of helper files (a single JavaScript include with all Viewer SDK components used by this particular viewer, assets, CSS) downloaded by the viewer in runtime.

You can use Zoom Viewer in pop-up mode using a production-ready HTML page provided with IS-Viewers or in embedded mode, where it is integrated into target web page using documented API.

Configuration and skinning are similar to that of the other viewers. All skinning is achieved by way of custom CSS.

See [Command reference common to all viewers - Configuration attributes](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) and [Command reference common to all Viewers - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interacting with Zoom Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

Zoom Viewer supports the following touch gestures that are common in other mobile applications. When the viewer cannot process user's swipe gesture, it forwards the event to the web browser to perform native page scroll. This kind of functionality lets the user navigate through the page even if the viewer occupies most of the device screen area.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Gesture </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Single tap </p> </td> 
   <td colname="col2"> <p> Selects new thumbnail in swatches. In the main view, it hides or reveals user interface elements. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Double tap </p> </td> 
   <td colname="col2"> <p> Zooms in one level until maximum magnification is reached. The next double tap gesture resets the viewer to the initial viewing state. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pinch </p> </td> 
   <td colname="col2"> <p>Zooms in or out. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Horizontal swipe or flick </p> </td> 
   <td colname="col2"> <p> Scrolls through the list of swatches in the swatch bar. </p> <p> If the image is in a reset state and the <span class="codeph"> frametransition </span> parameter is set to slide, the asset is changed with the slide animation. For other <span class="codeph"> frametransition </span> modes, the gesture performs native page scrolling. </p> <p> If the image is zoomed in, it moves the image horizontally. If image is moved to the view edge and a swipe is performed in the same direction, the gesture performs native page scrolling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vertical swipe </p> </td> 
   <td colname="col2"> <p> If the image is in a reset state, the gesture performs native page scrolling. </p> <p> When the image is zoomed in, it moves the image vertically. If the image is moved to the view edge and a swipe is performed in the same direction, the gesture performs native page scroll. </p> <p> If the gesture is done within the swatches area, it performs a native page scroll. </p> </td> 
  </tr> 
 </tbody> 
</table>

The viewer supports both touch input and mouse input on Windows devices with a touch screen and mouse. This support, however, is limited to Chrome, Internet Explorer 11, and Edge web browsers only.

This viewer is fully keyboard accessible.

See [Keyboard accessibility and navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Embedding Zoom Viewer {#section-6bb5d3c502544ad18a58eafe12a13435}

Different web pages have different needs for viewer behavior. Sometimes a web page provides a link that, when selected, opens the viewer in a separate browser window. In other cases, it is necessary to embed the viewer directly in the hosting page. In the latter case, the web page may have static layout, or use responsive design that displays differently on different devices or for different browser window sizes. To accommodate these needs, the viewer supports three primary operation modes: pop-up, fixed size embedding, and responsive design embedding.

**About pop-up mode**

In pop-up mode, the viewer is opened in a separate web browser window or tab. It takes the entire browser window area and adjusts in case the browser is resized or the device orientation is changed.

This mode is the most common for mobile devices. The web page loads the viewer using `window.open()` JavaScript call, properly configured `A` HTML element, or any other suitable method.

It is recommended that you use an out-of-the-box HTML page for the pop-up operation mode. The out-of-the-box HTML page is called `ZoomViewer.html` and it is located under the `html5/` subfolder of your standard IS-Viewers deployment as in the following:

`<s7viewers_root>/html5/ZoomViewer.html`

Apply custom CSS to achieve a customized appearance for the page.

The following is an example of HTML code that opens the viewer in the new window:

```html {.line-numbers}
 <a href="http://s7d1.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample" 
target="_blank">Open popup viewer</a>
```

**About fixed size embedding mode and responsive design embedding mode**

In the embedded mode the viewer is added to the existing web page, which may already have some customer content not related to the viewer. The viewer normally occupies only a part of the web page's real estate.

The primary use cases are web pages oriented for desktops or tablet devices, and also responsive designed pages that adjust layout automatically, depending on the device type.

Fixed size embedding is used when the viewer does not change its size after initial load. This option is the best choice for web pages that have a static layout.

Responsive design embedding mode assumes that the resizing of the viewer is necessary during runtime due to the size change of its container `DIV`. The most common use case is adding a viewer to a web page that uses a flexible layout.

In responsive design embedding mode, the viewer behaves differently depending on the way web page sizes its container `DIV`. If the web page only sets the width of the container `DIV`, leaving its height unrestricted, the viewer automatically chooses its height according to the aspect ratio of the asset that is used. This logic ensures that the asset fits perfectly into the view without any padding on the sides. This use case is the most common for web pages that use responsive layout frameworks such as Bootstrap and Foundation.

If the web page sets both the width and the height for the viewer's container `DIV`, the viewer fills that area and follows the size that the web page provides. For example, embedding the viewer into a modal overlay, where the overlay is sized according to web browser window size.

## Fixed size embedding {#section-44f365e6c0dd40709467a459afa82a7f}

You add the viewer to a web page by doing the following:

1. Adding the viewer JavaScript file to your web page. 
1. Defining the container DIV. 
1. Setting the viewer size. 
1. Creating and initializing the viewer.

1. Adding the viewer JavaScript file to your web page.

   Creating a viewer requires that you add a script tag in the HTML head. Before you can use the viewer API, be sure that you include [!DNL ZoomViewer.js]. The [!DNL ZoomViewer.js] file is located under the [!DNL html5/js/] subfolder of your standard IS-Viewers deployment:

[!DNL <s7viewers_root>/html5/js/ZoomViewer.js]

   You can use a relative path if the viewer is deployed on one of the Adobe Dynamic Media Classic servers and it is served from the same domain. Otherwise, you specify a full path to one of Adobe Dynamic Media Classic servers that have the IS-Viewers installed.

   The relative path looks like the following:

   ```html {.line-numbers}
   <script language="javascript" type="text/javascript" src="/s7viewers/html5/js/ZoomViewer.js"></script>
   ```

   >[!NOTE]
   >
   >Only reference the main viewer JavaScript `include` file on your page. Do not reference any additional JavaScript files in the web page code which might be downloaded by the viewer's logic in runtime. In particular, do not directly reference HTML5 SDK `Utils.js` library loaded by the viewer from `/s7viewers` context path (so-called consolidated SDK `include`). The reason is that the location of `Utils.js` or similar runtime viewer libraries is fully managed by the viewer's logic and the location changes between viewer releases. Adobe does not keep older versions of secondary viewer `includes` on the server. 
   >
   >
   >As a result, putting a direct reference to any secondary JavaScript `include` used by the viewer on the page breaks the viewer functionality in the future when a new product version is deployed.

1. Defining the container DIV.

   Add an empty DIV element to the page where you want the viewer to appear. The DIV element must have its ID defined because this ID is passed later to the viewer API.

   The placeholder DIV is a positioned element, meaning that the `position` CSS property is set to `relative` or `absolute`.

   The following is an example of a defined placeholder DIV element:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Setting the viewer size.

   This viewer displays thumbnails when working with multi-item sets, on desktop systems thumbnails are placed below the main view. At the same time, the viewer allows the swapping of the main asset in runtime using `setAsset()` API. As a Developer, you have control over how the viewer manages the thumbnails area at the bottom when the new asset has only one item. It is possible to keep the outer viewer size intact and let the main view increase its height and occupy thumbnails area. Or, you can keep the main view size static and collapse the outer viewer area, letting web page content to move up, and use free screen real estate leftover from the thumbnails.

   To keep the outer viewer bounds intact, define the size for the `.s7zoomviewer` top-level CSS class in absolute units. Sizing in CSS can be put right on the HTML page. Or, it can be put in a custom viewer CSS file, which is later assigned to a viewer preset record in Dynamic Media Classic or passed explicitly using a style command.

   See [Customizing Zoom Viewer](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-customizingviewer/c-html5-20-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) for more information about styling the viewer with CSS.

   The following is an example of defining a static outer viewer size in HTML page:

   ```html {.line-numbers}
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   You can see the behavior with a fixed outer viewer in the following example. Notice that when you switch between sets, the outer viewer size does not change:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html)

   To make the main view dimensions static, define the viewer size in absolute units for the inner `Container` SDK component using the `.s7zoomviewer` `.s7container` CSS selector, or by using `stagesize` modifier.

   The following is an example of defining the viewer size for the inner `Container` SDK component so that the main view area does not change its size when switching the asset:

   ```html {.line-numbers}
   #s7viewer.s7zoomviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   The following demo page shows the viewer behavior with a fixed main view size. Notice that when you switch between sets, the main view remains static and the web page content moves vertically.

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html)

   You can set the `stagesize` modifier in the viewer preset record in Dynamic Media Classic. Or, you can pass it explicitly with the viewer initialization code with the `params` collection or as an API call as described in the Command Reference section of this Help, as in the following:

   ```html {.line-numbers}
    zoomViewer.setParam("stagesize", 
   "640,480");
   ```

   A CSS-based approach is recommended and is used in this example. 

1. Creating and initializing the viewer.

   When you have completed the steps above, you create an instance of `s7viewers.ZoomViewer` class, pass all configuration information to its constructor and call `init()` method on a viewer instance.

   Configuration information is passed to the constructor as a JSON object. At minimum, this object should have `containerId` field which holds the name of the viewer container ID and nested `params` JSON object with configuration parameters that the viewer supports. In this case, the `params` object must have at least the Image Serving URL passed as `serverUrl` property and the initial asset as `asset` parameter. The JSON-based initialization API lets you create and start the viewer with a single line of code.

   It is important to have the viewer container added to the DOM so that the viewer code can find the container element by its ID. Some browsers delay building DOM until the end of the web page. For maximum compatibility, call the `init()` method just before the closing `BODY` tag, or on the body `onload()` event.

   At the same time, the container element should not necessarily be part of the web page layout yet. For example, it may be hidden using `display:none` style assigned to it. In this case, the viewer delays its initialization process until the moment when the web page brings the container element back to the layout. When this action occurs, the viewer load automatically resumes.

   The following is an example of creating a viewer instance, passing the minimum necessary configuration options to the constructor, and calling the `init()` method. This example assumes `zoomViewer` is the viewer instance, `s7viewer` is the name of placeholder DIV, `http://s7d1.scene7.com/is/image/` is the Image Serving URL, and `Scene7SharedAssets/ImageSet-Views-Sample` is the asset.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var zoomViewer = new s7viewers.ZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   The following code is a complete example of a trivial web page that embeds the Video Viewer with a fixed size:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var zoomViewer = new s7viewers.ZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

## Responsive design embedding with unrestricted height {#section-b9ca11a7e7aa4f74ab43244cbca37ae0}

With responsive design embedding, the web page normally has some kind of flexible layout in place that dictates the runtime size of the viewer's container `DIV`. For the following example, assume that the web page allows the viewer's container `DIV` to take 40% of the web browser window size, leaving its height unrestricted. The web page HTML code would look like the following:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html> 

```

Adding the viewer to such a page is similar to the steps for fixed size embedding. The only difference is that you do not need to explicitly define the viewer size.

1. Adding the viewer JavaScript file to your web page. 
1. Defining the container DIV. 
1. Creating and initializing the viewer.

All the steps above are the same as with the fixed size embedding. Add the container DIV to the existing `"holder"` DIV. The following code is a complete example. Notice how viewer size changes when the browser is resized, and how the viewer aspect ratio matches the asset.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html> 

```

The following examples page illustrates more real-life uses of responsive design embedding with unrestricted height:

[Live Demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## Flexible-size embedding with width and height defined {#section-3674e6c032594441a6576b7fb1de6e64}

If there is flexible-size embedding with width and height defined, the web page styling is different. It provides both sizes to the `"holder"` DIV and center it in the browser window. Also, the web page sets the size of the `HTML` and `BODY` element to 100 percent.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
html, body { 
 width: 100%; 
 height: 100%; 
} 
.holder { 
 position: absolute; 
 left: 20%; 
 top: 20%; 
 width: 60%; 
height: 60%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html> 

```

The rest of the embedding steps are identical to the steps used for responsive design embedding with unrestricted height. The resulting example is the following:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
<style type="text/css"> 
html, body { 
 width: 100%; 
 height: 100%; 
} 
.holder { 
 position: absolute; 
 left: 20%; 
 top: 20%; 
 width: 60%; 
height: 60%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html> 

```

## Embedding using setter-based API {#section-44e014925f24418b900696003855c0a9}

Instead of using JSON-based initialization, it is possible to use setter-based API and no-args constructor. Using this API constructor does not take any parameters and configuration parameters are specified using `setContainerId()`, `setParam()`, and `setAsset()` API methods with separate JavaScript calls.

The following example illustrates using fixed size embedding with setter-based API:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7zoomviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var zoomViewer = new s7viewers.ZoomViewer(); 
zoomViewer.setContainerId("s7viewer"); 
zoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
zoomViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
zoomViewer.init(); 
</script> 
</body> 
</html> 

```
