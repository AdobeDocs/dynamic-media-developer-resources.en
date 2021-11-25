---
title: Panoramic Viewer
description: HTML5 Panoramic Viewer is an image viewer that displays a panoramic image. The purpose of this viewer is to display a spherical panorama, also known as equirectangular image. It supports auto-panning and panning by gyroscopic movement.  It is designed to work on desktops and mobile devices.  Virtual reality viewing mode is available on supporting mobile devices.
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: 
---
# Panoramic{#panoramic}

HTML5 Panoramic Viewer is an image viewer that displays a panoramic image. The purpose of this viewer is to display a spherical panorama, also known as equirectangular image. It supports auto-panning and panning by gyroscopic movement.  It is designed to work on desktops and mobile devices.  Virtual reality viewing mode is available on supporting mobile devices.

See [System requirements and prerequisites](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).


Viewer type 514.

## Demo URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample](http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample)

## Using Panoramic Viewer {#section-f21ac23d3f6449ad9765588d69584772}

HTML5 Panoramic Viewer represents a main JavaScript file and a set of helper files (a single JavaScript include with all HTML5 Viewer SDK components used by this particular viewer, assets, CSS) downloaded by the viewer in runtime.
HTML5 Panoramic Viewer can be used both in popup mode using production-ready HTML page provided with IS-Viewers or in embedded mode, where it is integrated into target web page using documented API.
Configuration and skinning is similar to that of the other HTML5 viewers. All skinning can be achieved via custom CSS.

See [Command reference common to all viewers - Configuration attributes](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) and [Command reference common to all Viewers - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interacting with HTML5 Panoramic Viewer {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

HTML5 Panoramic Viewer supports auto-panning and navigation by drag or gyroscopic movement.

<table id="table_panoramic"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Navigation </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Desktop </p> </td> 
   <td colname="col2"> <p>Auto-pan and drag to navigate. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Touch device </p> </td> 
   <td colname="col2"> <p>Auto-pan and drag to navigate by default. Navigate by gyroscopic movement in VR render mode (vrrender=true).
 </p> </td> 
  </tr> 
 </tbody> 
</table>

The viewer supports both touch input and mouse input on Windows devices with touch screen and mouse, this support however is limited to Chrome, Internet Explorer 11 and Edge web browsers only.
Panoramic Viewer has the ability to render panoramic images in Virtual Reality (VR) mode by specifying the vrrender modifier.  When vrrender is enabled, a panoramic image will be displayed in split screens.  A common use case would be serving the image in a mobile phone mounted in a virtual reality headset, providing separate images for each eye.  The viewer will respond the gyroscopic movement of the head and navigate through the image.

## Embedding HTML5 Panoramic Viewer {#section-6bb5d3c502544ad18a58eafe12a13435}

Different web pages have different needs for viewer behavior. Sometimes a web page will provide a link, and clicking on that link opens the viewer in a separate browser window. In other cases, it may be necessary to embed the viewer right in the hosting page. In the latter case the web page may have static layout, or be "responsive" and display differently on different devices or for different browser window sizes. To accommodate these needs, the viewer supports three primary operation modes: popup, fixed size embedding and responsive embedding.

**About pop-up mode**

In the popup mode the viewer is opened in a separate web browser window or tab. It takes the whole browser window area and adjusts in case browser is resized or device orientation is changed.

This mode is the most common for mobile devices. The web page loads the viewer using window.open() JavaScript call, properly configured A HTML element or any other suitable way. 

It is recommended that you use an out-of-box HTML page for pop-up operation mode. It is called [!DNL PanoramicViewer.html] and it is located under the [!DNL html5/] subfolder of your standard IS-Viewers deployment:

[!DNL <s7viewers_root>/html5/PanoramicViewer.html]

Visual customization can be achieved by applying custom CSS.

Here is an example of HTML code which opens the viewer in the new window:

```
<a href="http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample" target="_blank">Open popup viewer</a>
```

**About fixed size embedding mode and responsive embedding mode**

In the embedded mode the viewer is added to the existing web page, which may already have some customer content not related to the viewer. The viewer normally occupies only a part of web page real estate.

The primary use case are web pages oriented for desktops or tablet devices, and also responsive web pages which adjust layout automatically depending on device type.

Fixed size embedding is used when viewer does not change its size after initial load. This is the best choice for web pages which have static layout.

Responsive embedding assumes that the viewer may need to resize in run time in response to the size change of its container DIV. The most common use case is adding viewer to a web page which uses flexible layout.

In responsive mode the viewer will behave differently depending on the way web page sizes its container DIV. If the web page sets only the width of the container DIV, leaving its height unrestricted, the viewer will automatically choose its height according to the aspect ratio of the asset being used; this will ensure the asset is perfectly fit into the view without any padding on the sides. This use case is the most common for web pages using responsive layout frameworks like Bootstrap, Foundation and such.

Otherwise, if the web page sets both the width and the height for the viewer's container DIV, the viewer will just fill that area and follow the size provided by web page layout. A good example may be embedding viewer into a modal overlay, where the overlay is sized according to web browser window size.


**Fixed size embedding**

You add the viewer to a web page by doing the following:

1. Adding the viewer JavaScript file to your web page. 
1. Defining the container `DIV`. 
1. Setting the viewer size. 
1. Creating and initializing the viewer.

1. Adding the viewer JavaScript file to your web page.

   Creating a viewer requires that you add a script tag in the HTML head. Before you can use the viewer API, be sure that you include [!DNL PanoramicViewer.js]. The [!DNL PanoramicViewer.js] file is located under the [!DNL html5/js/] subfolder of your standard IS-Viewers deployment:

[!DNL <s7viewers_root>/html5/js/PanoramicViewer.js]

   You can use a relative path if the viewer is deployed on one of the Adobe Dynamic Media Classic servers and it is served from the same domain. Otherwise, you specify a full path to one of Adobe Dynamic Media Classic servers that have the IS-Viewers installed.

   Relative path looks like the following:

   ```
   <script language="javascript" type="text/javascript" src="/s7viewers/html5/js/PanoramicViewer.js"></script>
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


   The following is an example of a defined placeholder DIV element:

   ```
   <div id="s7viewer" style="position:relative"></div> 
   
   ```

1. Setting the viewer size

   You can set the static size for the viewer by either declaring it for `.s7panoramicviewer` top-level CSS class in absolute units, or by using the modifier `stagesize`.

   Sizing in CSS can be put right on the HTML page, or in custom viewer CSS file, which is later assigned to a viewer preset record in AOD or passed explicitly using style command. Refer to Customizing the Viewer section for more information about styling the viewer with CSS. Below is an example of defining static viewer size in HTML page:
   
   ```
   #s7viewer.s7panoramicviewer {
     width: 1024px;
     height: 512px;
   }
   ```
   
   `stagesize` modifier can be passed explicitly with the viewer initialization code with params collection or as an API call as described in the Command Reference section, like this:
   
   ```
   panoramicViewer.setParam("stagesize", "512,256");
   ```
   
   CSS-based approach is recommended and will be used in this example.


1. Creating and initializing the viewer.

    When you have completed the steps above, you create an instance of `s7viewers.PanoramicViewer` class, pass all configuration information to its constructor and call `init(`) method on a viewer instance. Configuration information is passed to the constructor as a JSON object. At minimum, this object should have containerId field which holds the name of viewer container ID and nested params JSON object with configuration parameters supported by the viewer. In this case params object must have at least Image Serving URL passed as `serverUrl` property and initial asset as asset parameter. JSON-based initialization API lets you create and start the viewer with single line of code.

   It is important to have the viewer container added to the DOM so that the viewer code can find the container element by its ID. Some browsers delay building DOM until the end of the web page. For maximum compatibility, call the `init()` method just before the closing `BODY` tag, or on the body `onload()` event.

   At the same time, the container element should not necessarily be part of the web page layout yet. For example, it may be hidden using `display:none` style assigned to it. In this case, the viewer delays its initialization process until the moment when the web page brings the container element back to the layout. When this action occurs, the viewer load automatically resumes.

   The following is an example of creating a viewer instance, passing minimum necessary configuration options to the constructor, and calling the `init()` method. This example assumes `panoramicViewer` is the viewer instance, `s7viewer` is the name of placeholder `DIV`, [!DNL http://s7d1.scene7.com/is/image/] is the Image Serving URL, and [!DNL Scene7SharedAssets/PanoramicImage-Sample] is the asset.

   ```
   <script type="text/javascript"> 
   var panoramicViewer = new s7viewers.PanoramicViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
     "asset":"Scene7SharedAssets/PanoramicImage-Sample",
     "serverurl":"http://s7d1.scene7.com/is/image/"
   } 
   }).init(); 
   </script> 
   
   ```

   The following code is a complete example of a trivial web page that embeds the Panoramic Viewer with a fixed size:

   ```
   <!DOCTYPE html> 
   <html> 
    <head>
    <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
    <style type="text/css">
    #s7viewer.s7panoramicviewer {
        width: 1024px;
        height: 512px;
    }
    </style>
    </head>
    <body>
    <div id="s7viewer" style="position:relative"></div>
    <script type="text/javascript">
    var panoramicViewer = new s7viewers.PanoramicViewer({
        "containerId":"s7viewer",
    "params":{
        "asset":"Scene7SharedAssets/PanoramicImage-Sample",
        "serverurl":"http://s7d1.scene7.com/is/image/"
    }
    }).init();
    </script>
    </body>
    </html>
   
   ```

**Responsive design embedding with unrestricted height**

With the responsive embedding the web page normally has some kind of flexible layout in place which dictates the run-time size of the viewer's container DIV. For the purposes of this example let's assume that the web page allows viewer's container DIV to take 80% of the web browser window size, leaving its height unrestricted. The web page HTML code could look like this:

```
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
.holder {
	width: 80%;
}
</style>
</head>
<body>
<div class="holder"></div>
</body>
</html> 

```

Adding the viewer to such page is very similar to the fixed size embedding, with the only difference that you do not need to explicitly define viewer size:

1. Adding the viewer JavaScript file to your web page. 
1. Defining the container DIV. 
1. Creating and initializing the viewer.

All the steps above are the same as with the fixed size embedding. Container DIV should be added to the existing "holder" DIV. The following code is a complete example, you may see how viewer size changes when browser is resized, and how the viewer aspect ratio matches the asset.

```
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
<style type="text/css">
.holder {
	width: 80%;
}
</style>
</head>
<body>
<div class="holder">
<div id="s7viewer" style="position:relative"></div>
</div>
<script type="text/javascript">
var panoramicViewer = new s7viewers.PanoramicViewer({
	"containerId":"s7viewer",
"params":{
	"asset":"Scene7SharedAssets/PanoramicImage-Sample",
	"serverurl":"http://s7d1.scene7.com/is/image/"
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

The rest of embedding steps are identical to responsive embedding with unrestricted height. The resulting example is

```
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
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
var panoramicViewer = new s7viewers.PanoramicViewer({
	"containerId":"s7viewer",
"params":{
	"asset":"Scene7SharedAssets/PanoramicImage-Sample",
	"serverurl":"http://s7d1.scene7.com/is/image/"
}
}).init();
</script>
</body>
</html>

```

**Embedding using Setter-based API**

Instead of using JSON-based initialization, it is possible to use setter-based API and no-args constructor. With that API, constructor does not take any parameters and configuration parameters are specified using `setContainerId()`, `setParam()`, and `setAsset()` API methods with separate JavaScript calls.

The following example illustrates fixed size embedding with setter-based API:

```
<!DOCTYPE html>
<html>
<head>
<script language="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
<style type="text/css">
#s7viewer.s7panoramicviewer {
	width: 1024;
	height: 512;
}
</style>
</head>
<body>
<div id="s7viewer" style="position:relative"></div>
<script type="text/javascript">
var panoramicViewer = new s7viewers.PanoramicViewer();
panoramicViewer.setContainerId("s7viewer");
panoramicViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/");
panoramicViewer.setAsset("Scene7SharedAssets/PanoramicImage-Sample");
panoramicViewer.init();
</script>
</body>
</html>

```
