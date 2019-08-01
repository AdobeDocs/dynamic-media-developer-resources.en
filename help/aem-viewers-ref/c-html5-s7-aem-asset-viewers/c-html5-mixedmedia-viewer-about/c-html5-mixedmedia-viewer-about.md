---
description: Mixed Media Viewer is a media viewer. It supports media sets that contain images, swatch sets, spin sets, videos, and Adaptive Video Sets.
keywords: responsive
seo-description: Mixed Media Viewer is a media viewer. It supports media sets that contain images, swatch sets, spin sets, videos, and Adaptive Video Sets.
seo-title: Mixed Media
solution: Experience Manager
title: Mixed Media
topic: Dynamic media
uuid: b6028c54-7a3c-41eb-89f8-7b86bb0d0deb
index: y
internal: n
snippet: y
---

# Mixed Media{#mixed-media}

Mixed Media Viewer is a media viewer. It supports media sets that contain images, swatch sets, spin sets, videos, and Adaptive Video Sets.

A thumbnail at the bottom of the viewer represents each media set element, along with its asset type indicator. When a swatch set element is selected, a secondary row of swatches appears to allow the selection of color variation within the swatch set. Images and swatch set elements support zooming in continuous or inline mode; spin sets support both zooming and spinning. Videos and Adaptive Video Sets support all basic playback controls as long as any optional closed captions are displayed on top of the video content. A user can switch to full screen any time by clicking the full screen button. The viewer has optional close button. It is designed to work on desktops and mobile devices.

The Mixed Media Viewer uses HTML5 streaming video playback in HLS format in its default configuration whenever the underlying system supports that. On systems that do not support HTML5 streaming the viewer falls back to HTML5 progressive video delivery.

>[!NOTE]
>
>Images which use IR (Image Rendering) or UGC (User-Generated Content) are not supported by this viewer.

Viewer type 505.

See [System requirements and prerequisites](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Demo URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample](https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample)

## Using Mixed Media Viewer {#section-f21ac23d3f6449ad9765588d69584772}

Mixed Media Viewer represents a main JavaScript file and a set of helper files (a single JavaScript include with all Viewer SDK components used by this particular viewer, assets, CSS) downloaded by the viewer in runtime.

You can use the Mixed Media Viewer in pop-up mode using production-ready HTML page provided with IS-Viewers. Or, you can use the viewer in embedded mode, where it is integrated into a target web page using the documented API.

The task of configuring and skinning the viewer is similar to other viewers. All skinning is achieved by way of custom CSS.

See [Command reference common to all viewers - Configuration attributes](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) and [Command reference common to all Viewers - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interacting with Mixed Media Viewer {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Mixed Media Viewer supports single-touch and multi-touch gestures that are common in other mobile applications. When the viewer cannot process a user's swipe gesture it forwards the event to the web browser to perform a native page scroll. This functionality lets a user navigate through the page even if the viewer occupies most of the device screen area.

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
   <td colname="col2"> <p> Activates the flyout view or changes between the primary and secondary zoom level. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Double tap </p> </td> 
   <td colname="col2"> <p>When in <span class="codeph"> continuous </span> zoom mode, zooms in one level until maximum magnification is reached, the next double tap gesture resets to initial state. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Touch and hold </p> </td> 
   <td colname="col2"> <p> When in <span class="codeph"> inline </span> zoom mode, activates zoomed image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pinch </p> </td> 
   <td colname="col2"> <p>When in continuous zoom mode, zooms image in or out. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Horizontal swipe or flick </p> </td> 
   <td colname="col2"> <p> When the current asset is a spin set, and the image is in a reset state, it spins through the spin set horizontally. </p> <p> When the current asset is a spin set or an image and the image is zoomed in, it moves the image horizontally. If the image is moved to the view edge and swipe is still done in that direction, the gesture performs a native page scroll. </p> <p> Scrolls through the list of swatches in the swatch bar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vertical swipe or flick </p> </td> 
   <td colname="col2"> <p> If the image is in a reset state, it changes the vertical view angle in case a multi-dimensional spin set is used. In a one-dimensional spin set, or when a multi-dimensional spin set is on the last or first axis, so that vertical swipe does not result in vertical view angle change, the gesture performs native page scroll. </p> <p> When current asset is a spin set or an image and the image is zoomed in, moves the image vertically. If image is moved to the view edge and swipe is still done in that direction, the gesture performs native page scroll. </p> <p> If the gesture is done within the swatches area, it performs a native page scroll. </p> </td> 
  </tr> 
 </tbody> 
</table>

The viewer also supports both touch input and mouse input on Windows devices with touch screen and mouse. This support, however, is limited to Chrome, Internet Explorer 11, and Edge web browsers only.

This viewer is fully keyboard accessible.

See [Keyboard accessibility and navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Embedding Mixed Media Viewer {#section-6bb5d3c502544ad18a58eafe12a13435}

Different web pages have different needs for viewer behavior. Sometimes a web page provides a link that, when clicked, opens the viewer in a separate browser window. In other cases, it is necessary to embed the viewer right in the hosting page. In the latter case, the web page may have a static page layout, or use responsive design that displays differently on different devices or for different browser window sizes. To accommodate these needs, the viewer supports three primary operation modes: pop-up, fixed size embedding, and responsive design embedding.

## About pop-up mode {#section-77d5aa03b8b94566958a179b1a2cd474}

In pop-up mode, the viewer is opened in a separate web browser window or tab. It takes the entire browser window area and adjusts in case the browser is resized, or a mobile device's orientation is changed.

Pop-up mode is the most common for mobile devices. The web page loads the viewer using `window.open()` JavaScript call, properly configured `A` HTML element, or any other suitable method.

It is recommended that you use an out-of-the-box HTML page for pop-up operation mode. In this case, it is called [!DNL MixedMediaViewer.html] and is located within the [!DNL html5/] subfolder of your standard IS-Viewers deployment:

[!DNL <s7viewers_root>/html5/MixedMediaViewer.html]

You can achieve visual customization by applying custom CSS.

The following is an example of HTML code that opens the viewer in a new window:

```
<a href="http://s7d1.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample" target="_blank">Open popup viewer</a>
```

## About fixed size and responsive design embedding {#section-ec86b100ba5943d0b16694268520bbde}

In the embedded mode, the viewer is added to the existing web page, which may already have some customer content not related to the viewer. The viewer normally occupies only a part of a web page's real estate.

The primary use cases are web pages oriented for desktops or tablet devices, and also responsive design pages that adjust layout automatically depending on the device type.

Fixed size embedding is used when the viewer does not change its size after initial load. This is the best choice for web pages that have a static layout.

Responsive design embedding assumes that the viewer may need to resize at runtime in response to the size change of its container `DIV`. The most common use case is adding a viewer to a web page that uses a flexible page layout.

In responsive design embedding mode, the viewer behaves differently depending on the way web page sizes its container `DIV`. If the web page sets only the width of the container `DIV`, leaving its height unrestricted, the viewer automatically chooses its height according to the aspect ratio of the asset that is used. This functionality ensures that the asset fits perfectly into the view without any padding on the sides. This use case is the most common for web pages using responsive design layout frameworks like Bootstrap, Foundation, and so on.

Otherwise, if the web page sets both the width and the height for the viewer's container `DIV`, the viewer fills just that area and follows the size that the web page layout provides. A good example is embedding the viewer into a modal overlay, where the overlay is sized according to web browser window size.

## Fixed Size Embedding {#section-17d162f76ffa4804b27928f51e7bea1d}

You add the viewer to a web page by doing the following:

1. Adding the viewer JavaScript file to your web page. 
1. Defining the container `DIV`. 
1. Setting the viewer size. 
1. Creating and initializing the viewer.

1. Adding the viewer JavaScript file to your web page.

   Creating a viewer requires that you add a script tag in the HTML head. Before you can use the viewer API, be sure that you include [!DNL MixedMediaViewer.js]. The [!DNL MixedMediaViewer.js] file is located under the [!DNL html5/js/] subfolder of your standard IS-Viewers deployment:

[!DNL <s7viewers_root>/html5/js/MixedMediaViewer.js]

   You can use a relative path if the viewer is deployed on one of the Adobe Scene7 servers and it is served from the same domain. Otherwise, you specify a full path to one of Adobe Scene7 servers that have the IS-Viewers installed.

   The relative path looks like the following:

   ```
   <script language="javascript" type="text/javascript" src="/s7viewers/html5/js/MixedMediaViewer.js"></script>
   ```

   >[!NOTE]
   >
   >You should only reference the main viewer JavaScript `include` file on your page. You should not reference any additional JavaScript files in the web page code which might be downloaded by the viewer's logic in runtime. In particular, do not directly reference HTML5 SDK `Utils.js` library loaded by the viewer from `/s7viewers` context path (so-called consolidated SDK `include`). The reason is that the location of `Utils.js` or similar runtime viewer libraries is fully managed by the viewer's logic and the location changes between viewer releases. Adobe does not keep older versions of secondary viewer `includes` on the server. 
   >
   >
   >As a result, putting a direct reference to any secondary JavaScript `include` used by the viewer on the page breaks the viewer functionality in the future when a new product version is deployed.

1. Defining the container DIV.

   Add an empty DIV element to the page where you want the viewer to appear. The DIV element must have its ID defined because this ID is passed later to the viewer API. The DIV has its size specified through CSS.

   The placeholder DIV is a positioned element, meaning that the `position` CSS property is set to `relative` or `absolute`.

   Ensure that the full screen feature functions properly in Internet Explorer. Check to make sure that there are no other elements in the DOM that have a higher stacking order than your placeholder DIV.

   The following is an example of a defined placeholder DIV element:

   ```
   <div id="s7viewer" style="position:relative"></div> 
   
   ```

1. Setting the viewer size

   This viewer displays thumbnails when working with multi-item sets. On desktop systems, thumbnails are placed below the main view. At the same time, the viewer allows the swapping of the main asset during runtime using `setAsset()` API. As a developer, you have control over how the viewer manages the thumbnails area at the bottom when the new asset has only one item. It is possible to keep the outer viewer size intact and let the main view increase its height and occupy the thumbnails area. Or, you can keep the main view size static and collapse the outer viewer area, letting web page content to move up, and then use the free page real estate that is left from the thumbnails.

   To keep the outer viewer bounds intact define the size for `.s7mixedmediaviewer` top-level CSS class in absolute units. Sizing in CSS can be put right on the HTML page, or in a custom viewer CSS file, which is later assigned to a viewer preset record in Scene7 Publishing System, or passed explicitly using style command.

   See [Customizing Mixed Media Viewer](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#concept-61b3410f187c4bf3af09ec813c649bf4) for more information about styling the viewer with CSS.

   The following is an example of defining the static outer viewer size in an HTML page:

   ```
   #s7viewer.s7mixedmediaviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   You can see the behavior with a fixed outer viewer area on the following sample page. Notice that when you switch between sets, the outer viewer size does not change:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-outer-area.html)

   To make the main view dimensions static, define the viewer size in absolute units for the inner `Container` SDK component using `.s7mixedmediaviewer .s7container` CSS selector, or by using `stagesize` modifier.

   The following is an example of defining the viewer size for the inner `Container` SDK component so that the main view area does not change its size when switching the asset:

   ```
   #s7viewer.s7mixedmediaviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   The following sample page shows viewer behavior with a fixed main view size. Notice that when you switch between sets, the main view remains static and the web page content moves vertically:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-main-view.html)

   You can set the `stagesize` modifier either in the viewer preset record in Scene7 Publishing System, or pass it explicitly with the viewer initialization code with `params` collection, or as an API call as described in the Command Reference section of this Help, as in the following:

   ```
   mixedMediaViewer.setParam("stagesize", "640,480");
   ```

   A CSS-based approach is recommended and is used in this example. 

1. Creating and initializing the viewer.

   When you have completed the steps above, you create an instance of `s7viewers.MixedMediaViewer` class, pass all configuration information to its constructor and call `init()` method on a viewer instance. Configuration information is passed to the constructor as a JSON object. At minimum, this object should have the `containerId` field which holds the name of viewer container ID and nested `params` JSON object with configuration parameters that the viewer supports. In this case, the `params` object must have at least the Image Serving URL passed as `serverUrl` property, the video server URL passed as `videoserverurl` property and initial asset as `asset` parameter. JSON-based initialization API lets you create and start the viewer with single line of code.

   It is important to have the viewer container added to the DOM so that the viewer code can find the container element by its ID. Some browsers delay building DOM until the end of the web page. For maximum compatibility, call the `init()` method just before the closing `BODY` tag, or on the body `onload()` event.

   At the same time, the container element should not necessarily be part of the web page layout just yet. For example, it may be hidden using `display:none` style assigned to it. In this case, the viewer delays its initialization process until the moment when the web page brings the container element back to the layout. When this occurs, the viewer load automatically resumes.

   The following is an example of creating a viewer instance, passing the minimum necessary configuration options to the constructor, and calling the `init()` method. The example assumes `mixedMediaViewer` is the viewer instance; `s7viewer` is the name of placeholder `DIV`; [!DNL http://s7d1.scene7.com/is/image/] is the Image Serving URL; [!DNL http://s7d1.scene7.com/is/content/] is the video server URL; and [!DNL Scene7SharedAssets/Mixed_Media_Set_Sample] is the asset:

```
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
<script type="text/javascript"> 
mixedMediaViewer.init(); 
</script>
```

The following code is a complete example of a trivial web page that embeds the Mixed Media Viewer with a fixed size:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7mixedmediaviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## Responsive embedding with unrestricted height {#section-056cb574713c4d07be6d07cf3c598839}

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

Adding the viewer to such a page is similar to the steps for fixed size embedding. The only difference is that you do not need to explicitly define the viewer size.

1. Adding the viewer JavaScript file to your web page. 
1. Defining the container DIV. 
1. Creating and initializing the viewer.

All the steps above are the same as with the fixed size embedding. Add the container DIV to the existing `"holder"` DIV. The following code is a complete example. Notice how viewer size changes when the browser is resized, and how the viewer aspect ratio matches the asset.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
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
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

The following examples page illustrates more real-life uses of responsive design embedding with unrestricted height:

[https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html](https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html)

## Flexible size embedding with width and height defined {#section-0a329016f9414d199039776645c693de}

In case of flexible-size embedding with width and height defined, the web page styling is different. It provides both sizes to the `"holder"` DIV and centers it in the browser window. Also, the web page sets the size of the `HTML` and `BODY` element to 100 percent.

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
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
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7mixedmediaviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer(); 
mixedMediaViewer.setContainerId("s7viewer"); 
mixedMediaViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
mixedMediaViewer.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample"); 
mixedMediaViewer.init(); 
</script> 
</body> 
</html>
```

