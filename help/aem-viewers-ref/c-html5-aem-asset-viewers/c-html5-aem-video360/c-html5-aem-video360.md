---
description: The HTML5 Video360 Viewer is a 360-degree video player that plays streaming and progressive 360 video encoded in the H.264 format, delivered from Dynamic Media Classic or from AEM Dynamic Media.
solution: Experience Manager
title: Video360
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,Business Practitioner
exl-id: 74dca3f6-ce89-4c5b-8459-c2c4ca8ed27c
---
# Video360{#video}

The HTML5 Video360 Viewer is a 360-degree video player that plays streaming and progressive 360 video encoded in the H.264 format, delivered from Dynmaic Media Classic or from AEM Dynamic Media.

360-degree videos, also known as immersive videos or spherical videos, are video recordings where a view in every direction is recorded at the same time, shot using an omnidirectional camera or a collection of cameras. Both single video and Adaptive Video Sets are supported. The viewer additionally supports working with progressive video and HLS streams hosted on external location.

The recommended aspect ratio for 360 video is 2:1. Spatial sound is not supported. The viewer is designed to work with 360 video only; an attempt to play a non-360 video results in distorted video playback.

The viewer is designed to work on both desktop and mobile Web browsers that support HTML5 video. The viewer supports optional social sharing tools.

The Video360 Viewer uses HTML5 streaming video playback in HLS format in its default configuration whenever the underlying system supports that. On systems that do not support HTML5 streaming the viewer falls back to HTML5 progressive video delivery.

Viewer type is 517.

## Demo URLs {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## System Requirements {#section-b7270cc4290043399681dc504f043609}

See [System requirements](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Using Video360 Viewer {#section-e6c68406ecdc4de781df182bbd8088b4}

HTML5 Video360 Viewer represent a main JavaScript file and a set of helper files (a single JavaScript include with all HTML5 Viewer SDK components used by this particular viewer, assets, CSS) downloaded by the viewer in runtime.

HTML5 Video360 Viewer can be used both in popup mode using production-ready HTML page provided with IS-Viewers or in embedded mode, where it is integrated into target web page using documented API.

Configuration and skinning is similar to that of the other viewers described in this guide. All skinning is achieved by way of custom (CSS) Cascading Style Sheets.

See [Command reference common to all viewers - Configuration attributes](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) and [Command reference common to all Viewers - URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

360 video content requires higher encoding settings than the standard non-360 video. In other words, 360 content must come in higher resolution than non-360 video in order to achieve the same perceivable quality. It is recommended that you consider the following Adaptive Video Preset settings for 360 video:

* 720p, 2500 kbps 
* 1080p, 5000 kbps 
* 1440p, 6600 kbps

Note however that serving video encoded with such high quality settings requires a high bandwidth connection on an end user's device.

## Interacting with Video360 Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

HTML5 Video360 Viewer provides a set of standard user interface controls for video playback, like play/pause button, video scrubber video time bubble, played time/total time indicator, volume control and full screen button. All these controls are grouped into control bar in the very bottom of viewer user interface.

Note that on touch devices the volume control is hidden from the user interface, because it is only possible to control the volume using the device's hardware buttons.

When the viewer operates in pop-up mode, a full-screen button is not available in the user interface.

The viewer also supports a variety of social media sharing tools. They are available as a single button in the user interface which expands into a sharing toolbar when the user clicks or taps on it. The sharing toolbar contains an icon for each type of sharing channel supported such as Facebook, Twitter, email share, embed code share, and link share. When email share, embed share, or link share tools are activated, the viewer displays a modal dialog box with a corresponding data entry form. When Facebook or Twitter are called, the viewer redirects the user to a standard sharing dialog box from a social media service. Also, when a sharing tool is activated video playback is paused automatically. Sharing tools are not available in full-screen mode because of web browser security restrictions.

The viewer supports 360 video playback on VR headsets (like Oculus Go and Oculus Rift), VR HMD (head-mounted display) mounts (like Google Cardboard) and non-VR enabled devices (like desktop browsers, tablets and mobile phones not connected to VR HMD mounts).

No additional configuration is needed to view 360 video content on VR headset. The viewer automatically detects the presence of VR headset and shows "VR" button on top of video content. Activating this "VR" button switches video rendering to VR mode. The viewer supports VR rendering only in browsers with WebVR support.

In order to use VR HMD mounts the `Video360Player.vrrender` modifier must be set to `1` in viewer's configuration, which forces stereoscopic rendering.

On VR headsets and VR HMD mounts point of view change happens in response to headset movement, not other playback control is provided in VR mode.

When watching 360 video on non-VR enabled devices, end user can use mouse, touch or keyboard to control video playback and point of view.

The viewer supports both touch input and mouse input on Windows devices with touch screen and mouse, this support however is limited to Chrome, Internet Explorer 11 and Edge web browsers only.

The viewer is fully keyboard accessible. See [Keyboard accessibility and navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Embedding Video360 Viewer {#section-6bb5d3c502544ad18a58eafe12a13435}

Different web pages have different needs for viewer behavior. Sometimes a web page provides a link that, when clicked opens the viewer in a separate browser window. In other cases, it is necessary to embed the viewer directly on the hosting page. In the latter case the web page may have a static page layout, or use responsive design that displays differently on different devices or for different browser window sizes. To accommodate these needs, the viewer supports three primary operation modes: popup, fixed size embedding, and responsive design embedding.

Embedding multiple videos on the same page is supported on tablet and mobile devices. In a majority of cases, only one video can be played at a time. When a user starts playing one video, and then tries to play another video, the first video is automatically paused. The video that was auto-paused remembers its current playback time, so the user can always get back to it and resume play. The only exception this rule is in Chrome browser on Android 4.x devices, which can play videos in parallel.

**About pop-up mode**

In pop-up mode the viewer is opened in a separate web browser window or tab. It takes the entire browser window area and adjusts in case the browser is resized or device orientation is changed.

This mode is the most common for mobile devices. The web page loads the viewer using `window.open()` JavaScript call, properly configured `A` HTML element, or any other suitable method.

It is recommended that you use an out-of-box HTML page for pop-up operation mode. It is called [!DNL Video360Viewer.html] and it is located under the [!DNL html5/] subfolder of your standard IS-Viewers deployment:

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

You can achieve visual customization by applying custom CSS.

The following is an example of HTML code that opens the viewer in a new window:

```
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**About fixed size embedding mode and responsive design embedding mode**

In the embedded mode, the viewer is added to the existing web page, which may already have some customer content not related to the viewer. The viewer normally occupies only a part of a web page's real estate.

The primary use cases are web pages oriented for desktops or tablet devices, and also responsive designed pages that adjust layout automatically depending on the device type.

Fixed size embedding is used when the viewer does not change its size after initial load. This is the best choice for web pages that have a static layout.

Responsive design embedding assumes that the viewer may need to resize at runtime in response to the size change of its container `DIV`. The most common use case is adding a viewer to a web page that uses a flexible page layout.

In responsive design embedding mode, the viewer behaves differently depending on the way web page sizes its container `DIV`. If the web page sets only the width of the container `DIV`, leaving its height unrestricted, the viewer automatically chooses its height according to the aspect ratio of the asset that is used. This functionality ensures that the asset fits perfectly into the view without any padding on the sides. This use case is the most common for web pages using responsive web design layout frameworks like Bootstrap, Foundation, and so on.

Otherwise, if the web page sets both the width and the height for the viewer's container `DIV`, the viewer fills just that area and follows the size that the web page layout provides. A good example is embedding the viewer into a modal overlay, where the overlay is sized according to web browser window size.

**Fixed size embedding**

You add the viewer to a web page by doing the following:

1. Adding the viewer JavaScript file to your web page. 
1. Defining the container `DIV`. 
1. Setting the viewer size. 
1. Creating and initializing the viewer.

1. Adding the viewer JavaScript file to your web page.

   Creating a viewer requires that you add a script tag in the HTML head. Before you can use the viewer API, be sure that you include [!DNL Video360Viewer.js]. The [!DNL Video360Viewer.js] file is located under the [!DNL html5/js/] subfolder of your standard IS-Viewers deployment:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

   You can use a relative path if the viewer is deployed on one of the Adobe Dynamic Media Classic servers and it is served from the same domain. Otherwise, you specify a full path to one of Adobe Dynamic Media Classic servers that have the IS-Viewers installed.

   The relative path looks like the following:

   ```
   <script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
   ```

   >[!NOTE]
   >
   >You should only reference the main viewer JavaScript `include` file on your page. You should not reference any additional JavaScript files in the web page code which might be downloaded by the viewer's logic in runtime. In particular, do not directly reference HTML5 SDK `Utils.js` library loaded by the viewer from `/s7viewers` context path (so-called consolidated SDK `include`). The reason is that the location of `Utils.js` or similar runtime viewer libraries is fully managed by the viewer's logic and the location changes between viewer releases. Adobe does not keep older versions of secondary viewer `includes` on the server. 
   >
   >
   >As a result, putting a direct reference to any secondary JavaScript `include` used by the viewer on the page breaks the viewer functionality in the future when a new product version is deployed.

1. Defining the container `DIV`.

   Add an empty `DIV` element to the page where you want the viewer to appear. The `DIV` element must have its ID defined because this ID is passed later to the viewer API. The DIV has its size specified through CSS.

   The placeholder `DIV` is a positioned element, meaning that the `position` CSS property is set to `relative` or `absolute`.

   For the full-screen feature to function properly in Internet Explorer make sure that there are no other elements in the DOM that have a higher stacking order than your placeholder `DIV`.

   The following is an example of a defined placeholder `DIV` element:

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. Setting the viewer size

   You can set the static size for the viewer by either declaring it for `.s7video360viewer` top-level CSS class in absolute units, or by using `stagesize` modifier.

   You can put sizing in CSS directly on the HTML page, or in a custom viewer CSS file, which is then later assigned to a viewer preset record in AEM Assets - on-demand, or passed explicitly using `style` command.

   See [Customizing Video360 Viewer](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) for more information about styling the viewer with CSS.

   The following is an example of defining a static viewer size in the HTML page:

   ```
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   You can set the `stagesize` modifier in the viewer preset record in AEM Assets - on-demand. Or, you can pass it explicitly with the viewer initialization code with `params` collection, or as an API call as described in the Command Reference section, like this:

   ```
   video360viewer.setParam("stagesize", "640,640");
   ```

   A CSS-based approach is recommended and is used in this example. 

1. Creating and initializing the viewer.

   When you have completed the steps above, you create an instance of `s7viewers.Video360Viewer` class, pass all configuration information to its constructor, and call `init()` method on a viewer instance. Configuration information is passed to the constructor as a JSON object. At minimum, this object should have `containerId` field which holds the name of the viewer container ID and nested `params` JSON object with configuration parameters supported by the viewer.

   In this case, the `params` object must have at least the Image Serving URL passed as `serverUrl` property, and the initial asset as `asset` parameter. The JSON-based initialization API lets you create and start the viewer with a single line of code, video server URL passed as `videoserverurl` property, initial asset as `asset` parameter and interactive data as `interactivedata` property. JSON-based initialization API lets you create and start the viewer with single line of code.

   It is important to have the viewer container added to the DOM so that the viewer code can find the container element by its ID. Some browsers delay building DOM until the end of the web page. For maximum compatibility, call the `init()` method just before the closing `BODY` tag, or on the body `onload()` event.

   At the same, the container element should not necessarily be part of the web page layout just yet. For example, it may be hidden using `display:none` style assigned to it. In this case, the viewer delays its initialization process until the moment when the web page brings the container element back to the layout. When that happens, the viewer load automatically resumes.

   The following is an example of creating a viewer instance, passing the minimum necessary configuration options to the constructor and calling the `init()` method. The example assumes the following:

    * The viewer instance is `video360Viewer`. 
    * The name of placeholder `DIV` is `s7viewer`. 
    * The Image Serving URL is `https://s7d9.scene7.com/is/image`. 
    * The video server URL is `https://s7d9.scene7.com/is/content`. 
    * The asset is `Viewers/space_station_360-AVS`.

   ```
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
   } 
   }).init(); 
   </script>
   ```

   The following code is a complete example of a trivial web page that embeds the Video360 Viewer with a fixed size:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Responsive design embedding with unrestricted height**

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
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
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
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Responsive Embedding with Width and Height Defined**

In case of responsive embedding with width and height defined, the web page styling is different. It provides both sizes to the `"holder"` DIV and center it in the browser window. Also, the web page sets the size of the `HTML` and `BODY` element to 100 percent.

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

The rest of the embedding steps are identical to the steps used for responsive embedding with unrestricted height. The resulting example is the following:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
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
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Embedding Using Setter-based API**

Instead of using JSON-based initialization, it is possible to use setter-based API and no-args constructor. Using this API constructor does not take any parameters and configuration parameters are specified using `setContainerId()`, `setParam()`, and `setAsset()` API methods with separate JavaScript calls.

The following example illustrates using fixed size embedding with the setter-based API:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7video360viewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var video360Viewer = new s7viewers.Video360Viewer(); 
video360Viewer.setContainerId("s7viewer"); 
video360Viewer.setParam("serverurl", "https://s7d9.scene7.com/is/image/"); 
video360Viewer.setParam("videoserverurl", "https://s7d9.scene7.com/is/content/"); 
video360Viewer.setAsset("Viewers/space_station_360-AVS"); 
video360Viewer.init(); 
</script> 
</body> 
</html>
```
