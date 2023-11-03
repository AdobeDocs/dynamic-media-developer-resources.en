---
title: Smart Crop Video Viewer
description: The Smart Crop Video Viewer plays streaming and progressive video encoded in the H.264 format with the addition of smart crop support. It is delivered from Dynamic Media Classic or Adobe Experience Manager with Dynamic Media.
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 937be8a2-307e-47bb-9fc8-d354f780a214
---
# Smart Crop Video{#smart-crop-video}

The Smart Crop Video Viewer plays streaming and progressive video encoded in the H.264 format with the addition of smart crop support. It is delivered from Dynamic Media Classic or Experience Manager with Dynamic Media.

See [System requirements and prerequisites](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

Both single video and Adaptive Video Sets are supported. Also, the viewer supports working with progressive video and HLS streams hosted on external locations. It is designed to work on both desktop and mobile Web browsers that support HTML5 video. This viewer also supports optional closed captions that are displayed on top of video content, video chapter navigation, and social media sharing tools.

The Smart Crop Video Viewer uses HTML5 streaming video playback in HLS format in its default configuration whenever the underlying system supports it. On systems that do not support HTML5 streaming the viewer falls back to HTML5 progressive video delivery.

Viewer type 518.

## Demo URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS](https://s7d9.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS)

## Using Smart Crop Video Viewer {#section-f21ac23d3f6449ad9765588d69584772}

Smart Crop Video Viewer represents a main JavaScript file and a set of helper files-a single JavaScript include with all Viewer SDK components used by this particular viewer, assets, and CSS-downloaded by the viewer in runtime.

You can use the Smart Crop Video Viewer in pop-up mode using production-ready HTML page provided with IS-Viewers. Or, you can use the viewer in embedded mode, where it is integrated into a target web page using the documented API.

The task of configuring and skinning the viewer is similar to other viewers. All skinning is achieved by way of custom CSS.

See [Command reference common to all viewers - Configuration attributes](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) and [Command reference common to all Viewers - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interacting with Smart Crop Video Viewer {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Smart Crop Video Viewer provides a set of standard user interface controls for video playback, such as:

* A Play/Pause button.
* Video scrubber video time bubble.
* Played time/total time indicator.
* Volume control.
* full-screen button.
* Closed caption toggle.

All these controls are grouped into a control bar at the bottom of the viewer user interface.

On touch devices, volume control is hidden from the user interface, because it is only possible to control volume using the hardware buttons.

When the viewer operates in pop-up mode, the full-screen button is not available in the user interface.

It is possible to navigate the content of a video quickly when video chapter is activated. Video chapters are displayed as markers in the video scrubber track and show the chapter title and associated description on a mouse rollover or with a single tap on touch systems. Users can seek to a particular chapter by selecting a chapter marker or selecting the chapter description bubble.

The viewer supports both touch input and mouse input on Windows devices with touch screen and mouse. This support, however, is limited to Chrome, Internet Explorer 11, and Edge web browsers only.

This viewer is fully keyboard accessible.

See [Keyboard accessibility and navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Social media sharing tools with Smart Crop Video Viewer {#section-907d316fe1da4b87abb9775f02464704}

The Smart Crop Video Viewer supports social media sharing tools. They are available as a single button in the user interface which expands into a sharing toolbar when the user clicks or taps on it.

The sharing toolbar contains an icon for each type of sharing channel supported such as Facebook, Twitter, email share, embed code share and link share. When email share, embed share, or link share tools are activated, the viewer displays a modal dialog box with a corresponding data entry form. When Facebook or Twitter are called, the viewer redirects the user to a standard sharing dialog box from a social media service. Also when a sharing tool is activated video playback is paused automatically.

Sharing tools are not available in full-screen mode because of web browser security restrictions.

## Embedding Smart Crop Video Viewer {#section-6bb5d3c502544ad18a58eafe12a13435}

Different web pages have different needs for viewer behavior. Sometimes a web page provides a link that, when selected opens the viewer in a separate browser window. In other cases, it is necessary to embed the viewer directly on the hosting page. In the latter case, the web page may have a static page layout, or use responsive design that displays differently on different devices or for different browser window sizes. To accommodate these needs, the viewer supports three primary operation modes: popup, fixed size embedding, and responsive design embedding.

Embedding multiple videos on the same page is supported on tablet and mobile devices. Usually, only one video can be played at a time. When a user starts playing one video, and then tries to play another video, the first video is automatically paused. The video that was auto-paused remembers its current playback time, so the user can always get back to it and resume play. The only exception this rule is in Chrome browser on Android&trade; 4.x devices, which can play videos in parallel.

**About pop-up mode**

In pop-up mode, the viewer is opened in a separate web browser window or tab. It takes the entire browser window area and adjusts in case the browser is resized or device orientation is changed.

This mode is the most common for mobile devices. The web page loads the viewer using `window.open()` JavaScript call, properly configured `A` HTML element, or any other suitable method.

It is recommended that you use an out-of-box HTML page for pop-up operation mode. It is called [!DNL SmartCropVideoViewer.html] and it is located under the [!DNL html5/] subfolder of your standard IS-Viewers deployment:

[!DNL <s7viewers_root>/html5/SmartCropVideoViewer.html]

You can achieve visual customization by applying custom CSS.

The following is an example of HTML code that opens the viewer in a new window:

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS" target="_blank">Open popup viewer</a>
```

**About fixed size embedding mode and responsive embedding mode**

In the embedded mode, the viewer is added to the existing web page, which may already have some customer content not related to the viewer. The viewer normally occupies only a part of the web page's real estate.

The primary use cases are web pages oriented for desktops or tablet devices, and also responsive design pages that adjust layout automatically depending on the device type.

Fixed size embedding is used when viewer does not change its size after initial load. This choice is the best for web pages that have a static page layout.

Responsive design embedding assumes that the viewer must resize in run-time in response to the size change of its container `DIV`. The most common use case is adding the viewer to a web page that uses a flexible page layout.

In responsive design embedding mode, the viewer behaves differently depending on the way the web page sizes its container `DIV`. If the web page sets only the width of the container `DIV`, leaving its height unrestricted, the viewer automatically chooses its height according to the aspect ratio of the asset that is used. This method ensures that the asset fits perfectly into the view without any padding on the sides. This use case is the most common for web pages that use a responsive design layout framework like Bootstrap or Foundation.

Otherwise, if the web page sets both the width and the height for the viewer's container `DIV`, the viewer fills just that area and follows the size provided by web page layout. A good example is embedding the viewer into a modal overlay, where the overlay is sized according to the size of the web browser window.

**Fixed size embedding**

You add the viewer to a web page by doing the following:

1. Adding the viewer JavaScript file to your web page. 
1. Defining the container `DIV`. 
1. Setting the viewer size. 
1. Creating and initializing the viewer.

1. Adding the viewer JavaScript file to your web page.

   Creating a viewer requires that you add a script tag in the HTML head. Before you can use the viewer API, be sure that you include [!DNL SmartCropVideoViewer.js]. The [!DNL SmartCropVideoViewer.js] file is located under the [!DNL html5/js/] subfolder of your standard IS-Viewers deployment:

[!DNL <s7viewers_root>/html5/js/SmartCropVideoViewer.js]

   You can use a relative path if the viewer is deployed on one of the Adobe Dynamic Media Classic servers and it is served from the same domain. Otherwise, you specify a full path to one of Adobe Dynamic Media Classic servers that have the IS-Viewers installed.

   Relative path looks like the following:

   ```html {.line-numbers}
   <script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SmartCropVideoViewer.js"></script>
   ```

   >[!NOTE]
   >
   >Only reference the main viewer JavaScript `include` file on your page. Do not reference any additional JavaScript files in the web page code which might be downloaded by the viewer's logic in runtime. In particular, do not directly reference HTML5 SDK `Utils.js` library loaded by the viewer from `/s7viewers` context path (so-called consolidated SDK `include`). The reason is that the location of `Utils.js` or similar runtime viewer libraries is fully managed by the viewer's logic and the location changes between viewer releases. Adobe does not keep older versions of secondary viewer `includes` on the server. 
   >
   >
   >As a result, putting a direct reference to any secondary JavaScript `include` used by the viewer on the page breaks the viewer functionality in the future when a new product version is deployed.

1. Defining the container DIV.

   Add an empty DIV element to the page where you want the viewer to appear. The DIV element must have its ID defined because this ID is passed later to the viewer API. The DIV has its size specified through CSS.

   The placeholder DIV is a positioned element, meaning that the `position` CSS property is set to `relative` or `absolute`.

   Ensure that the full-screen feature functions properly in Internet Explorer. Check to make sure that there are no other elements in the DOM that have a higher stacking order than your placeholder DIV.

   The following is an example of a defined placeholder DIV element:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   
   ```

1. Setting the viewer size

   You can set the static size for the viewer by either declaring it for `.s7videoviewer` top-level CSS class in absolute units, or by using the modifier `stagesize`.

   You can put sizing in CSS right on the HTML page, or in a custom viewer CSS file. It is later assigned to a viewer preset record in Dynamic Media Classic or passed explicitly using a style command.

   See [Customizing Smart Crop Video Viewer](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) for more information about styling the viewer using CSS.

   The following is an example of defining a static viewer size in an HTML page:

   ```html {.line-numbers}
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   You can set `stagesize` modifier either in the viewer preset record in Dynamic Media Classic, or pass it explicitly with the viewer initialization code with `params` collection. Or, as an API call as described in the Command reference section, as in the following:

   ```html {.line-numbers}
   smartCropVideoViewer.setParam("stagesize", "640,480");
   ```

   A CSS-based approach is recommended and is used in this example. 

1. Creating and initializing the viewer.

   When you have completed the steps above, you create an instance of `s7viewers.SmartCropVideoViewer` class, pass all configuration information to its constructor, and call `init()` method on a viewer instance. Configuration information is passed to the constructor as a JSON object. At minimum, this object should have `containerId` field which holds the name of viewer container ID and nested `params` JSON object with configuration parameters supported by the viewer. In this case, `params` object must have at least the Image Serving URL passed as `serverUrl` property, video server URL passed as `videoserverurl` property, and the initial asset as `asset` parameter. The JSON-based initialization API lets you create and start the viewer with a single line of code.

   It is important to have the viewer container added to the DOM so that the viewer code can find the container element by its ID. Some browsers delay building DOM until the end of the web page. For maximum compatibility, call the `init()` method just before the closing `BODY` tag, or on the body `onload()` event.

   At the same time, the container element should not necessarily be part of the web page layout yet. For example, it may be hidden using `display:none` style assigned to it. In this case, the viewer delays its initialization process until the moment when the web page brings the container element back to the layout. When this action occurs, the viewer load automatically resumes.

   The following is an example of creating a viewer instance, passing minimum necessary configuration options to the constructor, and calling the `init()` method. This example assumes `smartCropVideoViewer` is the viewer instance, `s7viewer` is the name of placeholder `DIV`, [!DNL http://s7d1.scene7.com/is/image/] is the Image Serving URL, [!DNL http://s7d1.scene7.com/is/content/] is the video server URL, and [!DNL html5automation/frisbee-AVS] is the asset.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"html5automation/frisbee-AVS", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   
   ```

   The following code is a complete example of a trivial web page that embeds the Smart Crop Video Viewer with a fixed size:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"html5automation/frisbee-AVS", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   
   ```

**Responsive design embedding with unrestricted height**

With the responsive design embedding, the web page normally has some kind of flexible layout in place that dictates the run-time size of the viewer's container `DIV`. For purposes of this example, assume that the web page allows the viewer's container `DIV` to take 40% of the web browser window size, leaving its height unrestricted. The web page HTML code would look like the following:

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

Adding the viewer to such a page is similar to the fixed size embedding; the only difference is that you do not need to explicitly define the viewer size.

1. Adding the viewer JavaScript file to your web page. 
1. Defining the container DIV. 
1. Creating and initializing the viewer.

All the steps above are the same as with the fixed size embedding. Add container `DIV` to the existing " holder" `DIV`. The following code is a complete example. You can see how the viewer size changes when the browser is resized, and how the viewer aspect ratio matches the asset.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 

```

The following examples page illustrates more real-life use of responsive design embedding with unrestricted height:

[Live demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Alternate demo location](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**Responsive design embedding with width and height defined**

If there is responsive design embedding with width and height defined, the web page styling is different; it provides both sizes to the " holder" `DIV` and center it in the browser window. Also, the web page sets the size of the `HTML` and `BODY` element to 100%:

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

The remaining embedding steps are identical to responsive design embedding with unrestricted height. The resulting example is the following:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 

```

**Embedding using Setter-based API**

Instead of using JSON-based initialization, it is possible to use setter-based API and no-args constructor. With that API, constructor does not take any parameters and configuration parameters are specified using `setContainerId()`, `setParam()`, and `setAsset()` API methods with separate JavaScript calls.

The following example illustrates fixed size embedding with setter-based API:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7videoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer(); 
smartCropVideoViewer.setContainerId("s7viewer"); 
smartCropVideoViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
smartCropVideoViewer.setParam("videoserverurl", "http://s7d1.scene7.com/is/content/"); 
smartCropVideoViewer.setAsset("html5automation/frisbee-AVS"); 
smartCropVideoViewer.init(); 
</script> 
</body> 
</html> 

```
