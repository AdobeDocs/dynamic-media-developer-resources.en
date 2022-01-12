---
title: Inline Zoom
description: Inline Zoom Viewer is an image viewer. It displays a static image with the zoomed version shown over that static image when a user rolls over or touches the main view. This viewer works with image sets and navigation is done by using swatches. It is designed to work on desktops and mobile devices.
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 33e661b0-be5e-4d37-af88-47f7bc433c01
---
# Inline Zoom{#inline-zoom}

Inline Zoom Viewer is an image viewer. It displays a static image with the zoomed version shown over that static image when a user rolls over or touches the main view. This viewer works with image sets and navigation is done by using swatches. It is designed to work on desktops and mobile devices.

>[!NOTE]
>
>Images which use IR (Image Rendering) or UGC (User-Generated Content) are not supported by this viewer.

Viewer type is 504.

See [System requirements and prerequisites](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Demo URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&stagesize=500,400](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&stagesize=500,400)

## Using Inline Zoom Viewer {#section-f21ac23d3f6449ad9765588d69584772}

Inline Zoom Viewer represents a main JavaScript file and a set of helper files (a single JavaScript include with all Viewer SDK components used by this particular viewer, assets, CSS) downloaded by the viewer at runtime.

Inline Zoom Viewer can be used both in pop-up mode using production-ready HTML page provided with Image Serving Viewers or in embedded mode where it is integrated into a target web page using documented API.

Configuration and skinning are similar to that of the other viewers. You can use custom CSS to apply skinning.

See [Command reference common to all viewers - Configuration attributes](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) and [Command reference common to all Viewers - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interacting with Inline Zoom Viewer {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Inline Zoom Viewer supports single-touch and multi-touch gestures that are common in other mobile applications.

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
   <td colname="col2"> <p> Activates the flyout view or changes between the primary and secondary zoom level in swatches, selects new thumbnail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Horizontal swipe or flick </p> </td> 
   <td colname="col2"> <p> Scrolls through the list of swatches in the swatch bar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vertical swipe </p> </td> 
   <td colname="col2"> <p>If the gesture is done within the swatches area, it performs a native page scroll. </p> </td> 
  </tr> 
 </tbody> 
</table>

The viewer also supports both touch input and mouse input on Windows devices with touch screen and mouse. This support, however, is limited to Chrome, Internet Explorer 11, and Edge web browsers only.

This viewer is fully keyboard accessible.

See [Keyboard accessibility and navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Embedding Inline Zoom Viewer {#section-6bb5d3c502544ad18a58eafe12a13435}

Different web pages have different needs for viewer behavior. Sometimes a web page provides a clickable link that opens the viewer in a separate browser window. In other cases, it may be necessary to embed the viewer directly in the hosting page. In the latter case, the web page may have static page layout, or use responsive design that displays differently on different devices, or for different browser window sizes. To accommodate these needs, the viewer supports three primary operation modes: pop-up, fixed size embedding, and responsive embedding.

**Pop-up**

In the pop-up mode, the viewer is opened in a separate web browser window or tab. It takes the entire browser window area and adjusts when the browser window is resized or the device orientation is changed.

This mode is the most common for mobile devices. The web page loads the viewer using `window.open()` JavaScript call, properly configured `A` HTML element, or any other suitable way.

It is recommended that you use the out-of-the-box HTML page for pop-up mode called `FlyoutViewer.html`. It is located under the [!DNL html5/] subfolder of your standard Image Serving-Viewers deployment:

`<s7viewers_root>/html5/FlyoutViewer.html`

It is also necessary to have the FlyoutZoomView component configured to work in the inline zoom mode. It is recommended that you use the out-of-the-box `Scene7SharedAssets/Universal_HTML5_Zoom_Inline` preset for the Inline Zoom viewer, or a custom preset derived from it. Visual customization can be achieved by applying custom CSS.

The following is an HTML code example that opens the viewer in a new window:

```
 <a href="http://s7d1.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline"target="_blank">Open popup viewer</a>
```

**Fixed Size Embedding and Responsive Embedding**

In the embedded mode the viewer is added to the existing web page, which may already have some customer content not related to the viewer. The viewer normally occupies only a part of web page real estate.

The primary use cases are web pages oriented for desktops or tablet devices, and also responsive web pages which adjust layout automatically depending on the device type.

Fixed size embedding mode is used when the viewer does not change its size after its initial load. This choice is best for web pages that have a static page layout.

Responsive design embedding mode assumes that the viewer must resize during runtime in response to the size change of its container `DIV`. The most common use case is adding a viewer to a web page that uses a flexible page layout.

When using responsive design embedding mode with the Inline Zoom Viewer, make sure that you specify explicit breakpoints for the main view image using the `imagereload` parameter. Ideally, match your breakpoints with the viewer width breakpoints as dictated by the web page CSS.

In responsive design embedding mode, the viewer behaves differently depending on the way a web page container `DIV` is sized. If the web page sets only the width of the container `DIV`, leaving its height unrestricted, then the viewer automatically chooses its height according to the aspect ratio of the asset that is used. This functionality means that the asset fits perfectly into the view without any padding on the sides. This particular use case is the most common for web pages that use responsive design layout frameworks like Bootstrap or Foundation.

Otherwise, if the web page sets both the width and the height for the viewer's container `DIV`, then the viewer fills only that area and follows the size provided by the web page layout. A good use case example is embedding the viewer into a modal overlay, where the overlay is sized according to web browser window size.

**Fixed size embedding**

You add the viewer to a web page by doing the following:

1. Adding the viewer JavaScript file to your web page. 
1. Defining the container `DIV`. 
1. Setting the viewer size. 
1. Creating and initializing the viewer.

1. Adding the viewer JavaScript file to your web page.

   Creating a viewer requires that you add a script tag in the HTML head. Before you can use the viewer API, be sure that you include `FlyoutViewer.js`. `FlyoutViewer.js` is in the following [!DNL html5/js/] subfolder of your standard IS-Viewers deployment:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

   You can use a relative path if the viewer is deployed on one of the Adobe Dynamic Media servers and it is served from the same domain. Otherwise, you specify a full path to one of Adobe Dynamic Media servers that have the IS-Viewers installed.

   A relative path looks like the following:

   ```
   <script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
   ```

   >[!NOTE]
   >
   >Only reference the main viewer JavaScript `include` file on your page. Do not reference any additional JavaScript files in the web page code which might be downloaded by the viewer's logic in runtime. In particular, do not directly reference HTML5 SDK `Utils.js` library loaded by the viewer from `/s7viewers` context path (so-called consolidated SDK `include`). The reason is that the location of `Utils.js` or similar runtime viewer libraries is fully managed by the viewer's logic and the location changes between viewer releases. Adobe does not keep older versions of secondary viewer `includes` on the server. 
   >
   >
   >As a result, putting a direct reference to any secondary JavaScript `include` used by the viewer on the page breaks the viewer functionality in the future when a new product version is deployed.

1. Defining the container DIV.

   Add an empty DIV element to the page where you want the viewer to appear. The DIV element must have its ID defined because this ID is later passed to the viewer API.

   The placeholder DIV is a positioned element, meaning that the `position` CSS property is set to `relative` or `absolute`.

   It is the responsibility of the web page to specify the proper `z-index` for the placeholder DIV element. Doing so ensures that the viewer’s flyout portion appears on top of the other web page elements.

   The following is an example of a defined placeholder DIV element:

   ```
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   
   ```

1. Setting the viewer size.

   This viewer displays thumbnails when working with multi-item sets. On desktop systems, thumbnails are placed below the main view. At the same time, the viewer allows the swapping of the main asset during runtime using `setAsset()` API. As a developer, you have control over how the viewer manages the thumbnails area in the bottom area when the new asset has only one item. It is possible to keep the outer viewer size intact and let the main view increase its height and occupy the thumbnails area. Or, you can keep the main view size static and collapse the outer viewer area, letting web page content to move up, and then use the free page real estate left from the thumbnails.

   To keep the outer viewer bounds intact, define the size for `.s7flyoutviewer` top-level CSS class in absolute units. Sizing in CSS can be put right on the HTML page, or in a custom viewer CSS file, and later assigned to a viewer preset record in Dynamic Media Classic, or passed explicitly using style command.

   See [Customizing Inline Zoom Viewer](../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-customizingviewer/c-html5-inlinezoom-viewer-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) for more information about styling the viewer with CSS.

   The following is an example of defining the static outer viewer size in an HTML page:

   ```
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   You can see the behavior with a fixed outer viewer area on the following sample page. Notice that when you switch between sets, the outer viewer size does not change:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-outer-area.html)

   To make the main view dimensions static, define the viewer size in absolute units for the inner `Container` SDK component using `.s7flyoutviewer .s7container` CSS selector. In addition, you should override the fixed size defined for the `.s7flyoutviewer` top-level CSS class in the default viewer CSS, by setting it to `auto`.

   The following is an example of defining the viewer size for the inner `Container` SDK component so that the main view area does not change its size when switching the asset:

   ```
   #s7viewer.s7flyoutviewer { 
    width: auto; 
    height: auto; 
   }  
   #s7viewer.s7flyoutviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   The following sample page shows viewer behavior with a fixed main view size. Notice that when you switch between sets, the main view remains static and the web page content moves vertically:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-main-view.html)

   Also, the default viewer CSS provides a fixed size for its outer area out-of-the-box. 

1. Creating and initializing the viewer.

   When you have completed the steps above, you create an instance of `s7viewers.FlyoutViewer` class, pass all configuration information to its constructor and call `init()` method on a viewer instance. Configuration information is passed to the constructor as a JSON object. At minimum, this object should have the `containerId` field which holds the name of viewer container ID and nested `params` JSON object with configuration parameters that the viewer supports. In this case, the `params` object must have at least the Image Serving URL passed as `serverUrl` property; the initial asset as `asset` parameter, base path for loading CSS as `contentUrl` parameter, and preset name as `config` parameter. JSON-based initialization API lets you create and start the viewer with single line of code.

   It is important to have the viewer container added to the DOM so that the viewer code can find the container element by its ID. Some browsers delay building DOM until the end of the web page. For maximum compatibility, call the `init()` method just before the closing `BODY` tag, or on the body `onload()` event.

   At the same time, the container element should not necessarily be part of the web page layout yet. For example, it may be hidden using `display:none` style assigned to it. In this case, the viewer delays its initialization process until the moment when the web page brings the container element back to the layout. When this action happens, the viewer load automatically resumes.

   The following is an example of creating a viewer instance, passing the minimum necessary configuration options to the constructor and calling the `init()` method. The example assumes `inlineZoomViewer` is the viewer instance; `s7viewer` is the name of placeholder `DIV`; `http://s7d1.scene7.com/is/image/` is the Image Serving URL; and `Scene7SharedAssets/ImageSet-Views-Sample` is the asset:

   ```
   <script type="text/javascript"> 
   var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
   "config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
   "contenturl" : "http://s7d1.scene7.com/is/content/", 
   "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   The following code is a complete example of a trivial web page that embeds the Inline Zoom Viewer with a fixed size:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head><body> 
   <div id="s7viewer" style="position:relative;z-index:1;"></div> 
   <script type="text/javascript"> 
   var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
   "config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
   "contenturl" : "http://s7d1.scene7.com/is/content/", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

## Responsive design embedding with unrestricted height {#section-056cb574713c4d07be6d07cf3c598839}

With responsive design embedding, the web page normally has some kind of flexible layout in place that dictates the runtime size of the viewer's container `DIV`. For the following example, assume that the web page allows the viewer's container `DIV` to take 40% of the web browser window size, leaving its height unrestricted. The web page HTML code would look like the following:

```
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

Adding the viewer to such a page is similar to the steps for fixed size embedding. The only difference is that you must override the fixed sizing from the default viewer CSS with the size set in relative units.

1. Adding the viewer JavaScript file to your web page. 
1. Defining the container `DIV`. 
1. Setting the viewer size. 
1. Creating and initializing the viewer.

All the steps above are the same as with the fixed size embedding with the following three exceptions:

* add the container `DIV` to the existing "holder" `DIV`; 
* added `imagereload` parameter with explicit breakpoints; 
* instead of setting a fixed viewer size using absolute units use CSS that sets the viewer `width` and `height` to 100% as in the following:

```
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

The following code is a complete example. Notice how the viewer size changes when the browser is resized, and how the viewer aspect ratio matches the asset.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

The following examples page illustrates more real-life uses of responsive design embedding with unrestricted height:

[Live demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Alternate demo location](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

## Flexible size embedding with width and height defined {#section-0a329016f9414d199039776645c693de}

If there is flexible-size embedding with width and height defined, the web page styling is different. It provides both sizes to the `"holder"` DIV and centers it in the browser window. Also, the web page sets the size of the `HTML` and `BODY` element to 100 percent.

```
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

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
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
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## Embedding using Setter-based API {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

Instead of using JSON-based initialization, it is possible to use setter-based API and no-args constructor. Using this API constructor does not take any parameters and configuration parameters are specified using `setContainerId()`, `setParam()`, and `setAsset()` API methods, with separate JavaScript calls.

The following example illustrates using fixed size embedding with setter-based API:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7flyoutviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head><body> 
<div id="s7viewer" style="position:relative;z-index:1;"></div> 
<script type="text/javascript"> 
var inlineZoomViewer = new s7viewers.FlyoutViewer(); 
inlineZoomViewer.setContainerId("s7viewer"); 
inlineZoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
inlineZoomViewer.setParam("config", "Scene7SharedAssets/Universal_HTML5_Zoom_Inline"); 
inlineZoomViewer.setParam("contenturl", "http://s7d1.scene7.com/is/content/"); 
inlineZoomViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
inlineZoomViewer.init(); 
</script> 
</body> 
</html>
```
