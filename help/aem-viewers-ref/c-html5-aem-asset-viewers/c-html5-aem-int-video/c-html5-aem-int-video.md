---
title: Interactive Video
description: Interactive Video Viewer is a video player that plays streaming and progressive video encoded in the H.264 format.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: e54b0b1f-b015-4592-82e2-99f5080543e3
---
# Interactive Video{#interactive-video}

Interactive Video Viewer is a video player that plays streaming and progressive video encoded in the H.264 format.

The viewer also shows interactive product swatches next to the video content. Both single video and Adaptive Video Sets are supported. It is designed to work on both desktop and mobile Web browsers that support HTML5 video. The viewer supports optional closed captions displayed on top of video content, video chapter navigation, and social sharing tools. The purpose of this viewer is to help you implement a "shoppable video" experience. That is, users can select a swatch associated with a particular video time region and get redirected to a Quickview or a product detail page on the customer's website.

Viewer type is 510.

## Demo URLs {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/glacier/InteractiveVideoViewerDemo.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/glacier/InteractiveVideoViewerDemo.html)

And

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/AXIS/index.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/AXIS/index.html)

## System Requirements {#section-b7270cc4290043399681dc504f043609}

See [System requirements](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Using Interactive Video Viewer {#section-e6c68406ecdc4de781df182bbd8088b4}

Interactive Video Viewer represents a main JavaScript file and a set of helper files downloaded by the viewer in runtime. A single JavaScript is included with all Viewer SDK components used by this particular viewer, assets, and CSS.

Interactive Video Viewer can be used in pop-up mode using production-ready HTML page provided with Image Serving Viewers. It can also be used in embedded mode, where it is integrated into the targeted web page using the documented API.

Configuring and skinning are similar to that of the other viewers described in this guide. All skinning is achieved by way of custom (CSS) Cascading Style Sheets.

See [Command reference common to all viewers - Configuration attributes](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) and [Command reference common to all Viewers - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interacting with Interactive Video Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

Interactive Video Viewer provides a set of standard user interface controls for video playback, such as a Play/Pause button, video scrubber, video time bubble, played time/total time indicator, volume control, full-screen button, and closed caption toggle. All of these controls are grouped into a control bar directly under the main view.

On touch devices, the volume control is hidden from the user interface, because it is only possible to control the volume using the device's hardware buttons.

When the viewer operates in pop-up mode, a full-screen button is not available in the user interface.

The viewer shows a panel with interactive swatches to the right of the video viewing area. The list of swatches automatically advances as the video plays, so that swatches corresponding to the current video region are shown. Clicking or tapping on a swatch triggers an action that was associated with such swatch during author time. Depending on how you set it up, the trigger may redirect to a different page on the web site. Or, it may pass product information back to the web page logic, which in turn can trigger the opening of a Quickview that shows related product content.

It is possible to navigate through the video content quickly when video chapter is activated. Video chapters are displayed as markers in the video scrubber track and show the chapter title and description on rollover (or on a single tap on touch systems). The customer can "seek" to a particular chapter by clicking a chapter marker or tapping a chapter description bubble.

The viewer also supports various social media sharing tools. They are available as a single button in the user interface which expands into a sharing toolbar when the user clicks or taps on it. The sharing toolbar contains an icon for each type of sharing channel supported such as Facebook, Twitter, email share, embed code share, and link share. When email share, embed share, or link share tools are activated, the viewer displays a modal dialog box with a corresponding data entry form. When Facebook or Twitter are called, the viewer redirects the user to a standard sharing dialog box from a social media service. Also, when a sharing tool is activated video playback is paused automatically. Sharing tools are not available in full-screen mode because of web browser security restrictions.

The viewer is fully keyboard accessible. See [Keyboard accessibility and navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Embedding Interactive Video Viewer {#section-6bb5d3c502544ad18a58eafe12a13435}

Interactive Video Viewer is embedded into the hosting page. Such a web page may have a static layout, or it may be "responsive" and display differently on different devices or for different browser window sizes.

To accommodate these needs, the viewer supports two primary operation modes: fixed size embedding and responsive embedding.

**About fixed size embedding mode and responsive design embedding mode**

In the embedded mode, the viewer is added to the existing web page, which may already have some customer content not related to the viewer. The viewer normally occupies only a part of a web page's real estate.

The primary use cases are web pages oriented for desktops or tablet devices, and also responsive designed pages that adjust layout automatically depending on the device type.

Fixed size embedding is used when the viewer does not change its size after initial load. This functionality is the best choice for web pages that have a static layout.

Responsive design embedding assumes that the viewer needs to resize at runtime in response to the size change of its container `DIV`. The most common use case is adding a viewer to a web page that uses a flexible page layout.

In responsive design embedding mode, the viewer behaves differently depending on the way web page sizes its container `DIV`. If the web page sets only the width of the container `DIV`, leaving its height unrestricted, the viewer automatically chooses its height according to the aspect ratio of the asset that is used. This functionality ensures that the asset fits perfectly into the view without any padding on the sides. This use case is the most common for web pages using responsive web design layout frameworks like Bootstrap and Foundation.

Otherwise, if the web page sets both the width and the height for the viewer's container `DIV`, the viewer fills just that area and follows the size that the web page layout provides. A good example is embedding the viewer into a modal overlay, where the overlay is sized according to web browser window size.

**Fixed size embedding**

You add the viewer to a web page by doing the following:

1. Adding the viewer JavaScript file to your web page. 
1. Defining the container `DIV`. 
1. Setting the viewer size. 
1. Creating and initializing the viewer.

1. Adding the viewer JavaScript file to your web page.

   Creating a viewer requires that you add a script tag in the HTML head. Before you can use the viewer API, be sure that you include [!DNL InterativeVideoViewer.js]. The [!DNL InteractiveVideoViewer.js] file is located under the [!DNL html5/js/] subfolder of your standard IS-Viewers deployment:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js]

   You can use a relative path if the viewer is deployed on one of the Adobe Dynamic Media Classic servers and it is served from the same domain. Otherwise, you specify a full path to one of Adobe Dynamic Media Classic servers that have the IS-Viewers installed.

   The relative path looks like the following:

   ```html {.line-numbers}
   <script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
   ```

   >[!NOTE]
   >
   >Only reference the main viewer JavaScript `include` file on your page. Do not reference any additional JavaScript files in the web page code which might be downloaded by the viewer's logic in runtime. In particular, do not directly reference HTML5 SDK `Utils.js` library loaded by the viewer from `/s7viewers` context path (so-called consolidated SDK `include`). The reason is that the location of `Utils.js` or similar runtime viewer libraries is fully managed by the viewer's logic and the location changes between viewer releases. Adobe does not keep older versions of secondary viewer `includes` on the server. 
   >
   >
   >As a result, putting a direct reference to any secondary JavaScript `include` used by the viewer on the page breaks the viewer functionality in the future when a new product version is deployed.

1. Defining the container `DIV`.

   Add an empty `DIV` element to the page where you want the viewer to appear. The `DIV` element must have its ID defined because this ID is passed later to the viewer API. The DIV has its size specified through CSS.

   The placeholder `DIV` is a positioned element, meaning that the `position` CSS property is set to `relative` or `absolute`.

   For the full-screen feature to function properly in Internet Explorer make sure that there are no other elements in the DOM that have a higher stacking order than your placeholder `DIV`.

   The following is an example of a defined placeholder `DIV` element:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Setting the viewer size

   You can set the static size for the viewer by either declaring it for `.s7interactivevideoviewer` top-level CSS class in absolute units, or by using `stagesize` modifier.

   You can put sizing in CSS directly on the HTML page. Or, you can put it in a custom viewer CSS file, which is then later assigned to a viewer preset record in Adobe Experience Manager Assets - On-demand, or passed explicitly using `style` command.

   See [Customizing Interactive Video Viewer](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) for more information about styling the viewer with CSS.

   The following is an example of defining a static viewer size in the HTML page:

   ```html {.line-numbers}
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   You can set the `stagesize` modifier in the viewer preset record in Experience Manager Assets - On-demand. Or, you can pass it explicitly with the viewer initialization code with `params` collection, or as an API call as described in the Command Reference section, like this:

   ```html {.line-numbers}
   interactivevideoviewer.setParam("stagesize", "640,640");
   ```

   A CSS-based approach is recommended and is used in this example. 

1. Creating and initializing the viewer.

   When you have completed the steps above, you create an instance of `s7viewers.InteractiveVideoViewer` class, pass all configuration information to its constructor, and call `init()` method on a viewer instance. Configuration information is passed to the constructor as a JSON object. At minimum, this object should have `containerId` field which holds the name of the viewer container ID and nested `params` JSON object with configuration parameters supported by the viewer.

   In this case, the `params` object must have at least the Image Serving URL passed as `serverUrl` property, and the initial asset as `asset` parameter. The JSON-based initialization API lets you create and start the viewer with a single line of code, video server URL passed as `videoserverurl` property, initial asset as `asset` parameter, and interactive data as `interactivedata` property. JSON-based initialization API lets you create and start the viewer with single line of code.

   It is important to have the viewer container added to the DOM so that the viewer code can find the container element by its ID. Some browsers delay building DOM until the end of the web page. For maximum compatibility, call the `init()` method just before the closing `BODY` tag, or on the body `onload()` event.

   At the same, the container element is not necessarily part of the web page layout yet. For example, it may be hidden using `display:none` style assigned to it. In this case, the viewer delays its initialization process until the moment when the web page brings the container element back to the layout. What that happens, the viewer load automatically resumes.

   The following is an example of creating a viewer instance, passing the minimum necessary configuration options to the constructor and calling the `init()` method. The example assumes the following:

    * The viewer instance is `interactiveVideoViewer`. 
    * The name of placeholder `DIV` is `s7viewer`. 
    * The Image Serving URL is `https://aodmarketingna.assetsadobe.com/is/image/`. 
    * The video server URL is `https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna`. 
    * The content URL is `https://aodmarketingna.assetsadobe.com/`. 
    * The asset is `/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4`. 
    * The interactive data is `is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt`.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
   "config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
    "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
    "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
    "contenturl":"https://aodmarketingna.assetsadobe.com/", 
   "interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
   } 
   }).init(); 
   </script>
   ```

   The following code is a complete example of a trivial web page that embeds the Interactive Video Viewer with a fixed size:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;"></div> 
   <script type="text/javascript"> 
   var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
   "config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
    "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
    "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
    "contenturl":"https://aodmarketingna.assetsadobe.com/", 
   "interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Responsive design embedding with unrestricted height**

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
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
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
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
} 
}).init(); 
</script> 
</body> 
</html>
```

The following examples page illustrates more real-life uses of responsive design embedding with unrestricted height:

[Live demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Alternate demo location](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**Responsive Embedding with Width and Height Defined**

If there is responsive embedding with width and height defined, the web page styling is different. It provides both sizes to the `"holder"` DIV and center it in the browser window. Also, the web page sets the size of the `HTML` and `BODY` element to 100 percent.

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

The rest of the embedding steps are identical to the steps used for responsive embedding with unrestricted height. The resulting example is the following:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
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
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Embedding Using Setter-based API**

Instead of using JSON-based initialization, it is possible to use setter-based API and no-args constructor. Using this API constructor does not take any parameters and configuration parameters are specified using `setContainerId()`, `setParam()`, and `setAsset()` API methods with separate JavaScript calls.

The following example illustrates using fixed size embedding with the setter-based API:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7interactivevideoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer(); 
interactiveVideoViewer.setContainerId("s7viewer"); 
interactiveVideoViewer.setParam("config", "/etc/dam/presets/viewer/Shoppable_Video_Dark"); 
interactiveVideoViewer.setParam("serverurl", "https://aodmarketingna.assetsadobe.com/is/image/"); 
interactiveVideoViewer.setParam("videoserverurl", "https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna"); 
interactiveVideoViewer.setParam("contenturl", "https://aodmarketingna.assetsadobe.com/"); 
interactiveVideoViewer.setParam("interactivedata", "is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt"); 
interactiveVideoViewer.setAsset("/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4"); 
interactiveVideoViewer.init(); 
</script> 
</body> 
</html>
```
