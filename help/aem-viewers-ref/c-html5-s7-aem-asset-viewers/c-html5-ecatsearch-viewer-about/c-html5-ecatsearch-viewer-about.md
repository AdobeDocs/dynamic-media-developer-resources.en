---
description: eCatalog Search Viewer is a catalog viewer that displays electronic brochures in a spread by spread or page by page manner. The eCatalog lets users navigate through the catalog using additional user interface elements or dedicated thumbnails mode. Users can also zoom in on every page for greater detail.
keywords: responsive
solution: Experience Manager
title: eCatalog Search
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 915e628e-65e7-44c6-a2aa-d4ae7ed03b8e
---
# eCatalog Search{#ecatalog-search}

eCatalog Search Viewer is a catalog viewer that displays electronic brochures in a spread by spread or page by page manner. The eCatalog lets users navigate through the catalog using additional user interface elements or dedicated thumbnails mode. Users can also zoom in on every page for greater detail.

This viewer works with ecatalogs and supports optional image maps and social sharing tools. It has zoom tools, catalog navigation tools, full-screen support, thumbnails, and an optional close button. The viewer also supports social sharing tools, Print, Download, and Favorites. It is designed to work on desktops and mobile devices.

The user can also do a keyword-based or phrase-based search over the catalog contents.

>[!NOTE]
>
>Images which use IR (Image Rendering) or UGC (User-Generated Content) are not supported by this viewer.

Viewer type 513.

See [System requirements and prerequisites](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

<!--
## Demo URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&serverUrl=https://s7d9.scene7.com/is/image/&config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&contenturl=https://s7d9.scene7.com/skins/&asset=Viewers/Pluralist&searchserverurl=https://s7search1.scene7.com/s7search/](https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&serverUrl=https://s7d9.scene7.com/is/image/&config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&contenturl=https://s7d9.scene7.com/skins/&asset=Viewers/Pluralist&searchserverurl=https://s7search1.scene7.com/s7search/)

-->

## Using eCatalog Viewer {#section-e6c68406ecdc4de781df182bbd8088b4}

eCatalog Search Viewer represents a main JavaScript file and a set of helper files (a single JavaScript include with all Viewer SDK components used by this particular viewer, assets, CSS) downloaded by the viewer in runtime

You can use eCatalog Search Viewer in pop-up mode using a production-ready HTML page provided with IS-Viewers or in embedded mode, where it is integrated into target web page using documented API.

Configuration and skinning are similar to that of the other viewers. All skinning is achieved by way of custom CSS.

See [Command reference common to all viewers - Configuration attributes](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) and [Command reference common to all Viewers - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interacting with eCatalog Search Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

eCatalog Search Viewer supports the following touch gestures that are common in other mobile applications.

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
   <td colname="col2"> <p> Selects new thumbnail in swatches. </p> </td> 
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
   <td colname="col2"> <p>Scrolls through the list of catalog pages if a slide frame transition is used. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vertical swipe or flick </p> </td> 
   <td colname="col2"> <p>When the image is in a reset state, it performs a native page scroll. </p> <p>When thumbnails are active, it scrolls the list of thumbnails. </p> </td> 
  </tr> 
 </tbody> 
</table>

It is possible to enable a realistic page flip animation effect for navigating between catalog pages. In such cases, a user can hold and drag a page corner and flip the page.

This viewer also supports both touch input and mouse input on Windows devices with a touch screen and mouse. This support, however, is limited to Chrome, Internet Explorer 11, and Edge web browsers only.

## Social media sharing tools with eCatalog Search Viewer {#section-eb575084a99647c3a9591f439f40b412}

The eCatalog Search Viewer supports social sharing tools. They are available as a button in the main control bar which expands into a sharing tool bar when a user clicks or taps on it.

The sharing tool bar contains icons for each type of sharing channel supported which includes Facebook, Twitter, email share, embed code share, and link share. When email share, embed share, or link share tools are activated, the viewer displays a modal dialog box with a corresponding data entry form. When Facebook or Twitter is called, the viewer redirects the user to a standard sharing dialog from a social service. Sharing tools are not available in full-screen mode because of web browser security restrictions.

The viewer's Search feature is available as a looking glass icon in the main toolbar. Clicking or tapping the icon activates the Search panel with an input field. After entering a keyword or phrase and pressing Enter, the viewer renders search results in the panel and highlights found words in the main view.

## Embedding eCatalog Search Viewer {#section-6bb5d3c502544ad18a58eafe12a13435}

Different web pages have different needs for viewer behavior. Sometimes a web page provides a link that, when selected, opens the viewer in a separate browser window. In other cases, it is necessary to embed the viewer right in the hosting page. In the latter case, the web page may have a static page layout, or use responsive design that displays differently on different devices or for different browser window sizes. To accommodate these needs, the viewer supports three primary operation modes: pop-up, fixed size embedding, and responsive design embedding.

**About pop-up mode**

In pop-up mode, the viewer is opened in a separate web browser window or tab. It takes the entire browser window area and adjusts in case the browser is resized, or a mobile device's orientation is changed.

Pop-up mode is the most common for mobile devices. The web page loads the viewer using `window.open()` JavaScript call, properly configured `A` HTML element, or any other suitable method.

It is recommended that you use an out-of-the-box HTML page for pop-up operation mode. In this case, it is called [!DNL eCatalogSearchViewer.html] and is located within the [!DNL html5/] subfolder of your standard IS-Viewers deployment:

[!DNL <s7viewers_root>/html5/eCatalogSearchViewer.html]

You can achieve visual customization by applying custom CSS.

<!--
The following is an example of HTML code that opens the viewer in a new window:

```html {.line-numbers}
<a href="https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&serverUrl=https://s7d9.scene7.com/is/image/&config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&contenturl=https://s7d9.scene7.com/skins/&asset=Viewers/Pluralist&searchserverurl=https://s7search1.scene7.com/s7search/" target="_blank">Open pop-up viewer</a>
```
-->

**About fixed size embedding mode and responsive design embedding mode**

In the embedded mode, the viewer is added to the existing web page, which may already have some customer content not related to the viewer. The viewer normally occupies only a part of a web page's real estate.

The primary use cases are web pages oriented for desktops or tablet devices, and also responsive designed pages that adjust layout automatically depending on the device type.

Fixed size embedding is used when the viewer does not change its size after initial load. This is the best choice for web pages that have a static layout.

Responsive design embedding assumes that the viewer may need to resize at runtime in response to the size change of its container `DIV`. The most common use case is adding a viewer to a web page that uses a flexible page layout.

In responsive design embedding mode, the viewer behaves differently depending on the way web page sizes its container `DIV`. If the web page sets only the width of the container `DIV`, leaving its height unrestricted, the viewer automatically chooses its height according to the aspect ratio of the asset that is used. This functionality ensures that the asset fits perfectly into the view without any padding on the sides. This use case is the most common for web pages using responsive layout frameworks like Bootstrap, Foundation, and so on.

Otherwise, if the web page sets both the width and the height for the viewer's container `DIV`, the viewer fills just that area and follows the size that the web page layout provides. A good example is embedding the viewer into a modal overlay, where the overlay is sized according to web browser window size.

**Fixed size embedding**

You add the viewer to a web page by doing the following:

1. Adding the viewer JavaScript file to your web page. 
1. Defining the container DIV. 
1. Setting the viewer size. 
1. Creating and initializing the viewer.

1. Adding the viewer JavaScript file to your web page.

   Creating a viewer requires that you add a script tag in the HTML head. Before you can use the viewer API, be sure that you include [!DNL eCatalogSearchViewer.js]. The [!DNL eCatalogSearchViewer.js] file is located under the [!DNL html5/js/] subfolder of your standard IS-Viewers deployment:

[!DNL <s7viewers_root>/html5/js/eCatalogSearchViewer.js]

   You can use a relative path if the viewer is deployed on one of the Adobe Dynamic Media servers and it is served from the same domain. Otherwise, you specify a full path to one of Adobe Dynamic Media servers that have the IS-Viewers installed.

   The relative path looks like the following:

   ```html {.line-numbers}
   <script language="javascript" type="text/javascript" src="/s7viewers/html5/js/eCatalogSearchViewer.js"></script>
   ```

1. Defining the container DIV.

   Add an empty DIV element to the page where you want the viewer to appear. The DIV element must have its ID defined because this ID is passed later to the viewer API.

   The placeholder DIV is a positioned element, meaning that the `position` CSS property is set to `relative` or `absolute`.

   The following is an example of a defined placeholder DIV element:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Setting the viewer size

   You can set the static size for the viewer by either declaring it for `.s7ecatalogsearchviewer` top-level CSS class in absolute units, or by using `stagesize` modifier.

   You can put sizing in CSS directly on the HTML page, or in a custom viewer CSS file, which is then later assigned to a viewer preset record in Dynamic Media Classic, or passed explicitly using a style command.

   See [Customizing eCatalog Viewer](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) for more information about styling the viewer with CSS.

   The following is an example of defining a static viewer size in HTML page:

   ```html {.line-numbers}
   #s7viewer.s7ecatalogsearchviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   You can set the `stagesize` modifier either in the viewer preset record in Dynamic Media Classic, or pass it explicitly with the viewer initialization code with `params` collection, or as an API call as described in the Command Reference section, like the following:

   ```html {.line-numbers}
   eCatalogSearchViewer.setParam("stagesize", 
   "640,480");
   ```

1. Initializing the viewer.

   When you have completed the steps above, you create an instance of `s7viewers.eCatalogSearchViewer` class, pass all configuration information to its constructor and call `init()` method on a viewer instance. Configuration information is passed to the constructor as a JSON object. At minimum, this object has the `containerId` field which holds the name of viewer container ID and nested `params` JSON object with configuration parameters supported by the viewer. In this case, the `params` object must have at least the Image Serving URL passed as `serverUrl` property, and the initial asset as `asset` parameter. JSON-based initialization API lets you create and start the viewer with single line of code.

   It is important to have the viewer container added to the DOM so that the viewer code can find the container element by its ID. Some browsers delay building DOM until the end of the web page. For maximum compatibility, however, call the `init()` method just before the closing `BODY` tag, or on the body `onload()` event.

   At the same the container element should not necessarily be part of the web page layout just yet. For example, it may be hidden using `display:none` style assigned to it. In this case, the viewer delays its initialization process until the moment when the web page brings the container element back to the layout. When this happens, the viewer load automatically resumes.

   The following is an example of creating a viewer instance, passing the minimum necessary configuration options to the constructor, and calling the `init()` method. The example assumes `eCatalogSearchViewer` is the viewer instance; `s7viewer` is the name of placeholder `DIV`; `https://s7d1.scene7.com/is/image/` is the Image Serving URL, and `Viewers/Pluralist` is the asset:

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"https://s7d1.scene7.com/is/image/", 
    "searchserverurl":"https://s7search1.scene7.com/s7search/" 
   } 
   }).init(); 
   </script>
   ```

   The following code is a complete example of a trivial web page that embeds the eCatalog Search Viewer with a fixed size:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7ecatalogsearchviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"https://s7d1.scene7.com/is/image/", 
    "searchserverurl":"https://s7search1.scene7.com/s7search/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Responsive design embedding with unrestricted height**

With responsive design embedding, the web page normally has some kind of flexible layout in place that dictates the runtime size of the viewer's container `DIV`. For purposes of this example, assume that the web page allows the viewer's container `DIV` to take 40% of the web browser window size, leaving its height unrestricted. The resulting web page HTML code looks like the following:

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

Adding the viewer to such a page is similar to fixed size embedding, with the only difference being that you do not need to explicitly define viewer size.

1. Adding the viewer JavaScript file to your web page. 
1. Defining the container DIV. 
1. Creating and initializing the viewer.

All the steps above are the same as with fixed size embedding. Add the container `DIV` to the existing " holder" `DIV`. The following code is a complete example. You can see how the viewer size changes when the browser is resized, and how the viewer aspect ratio matches the asset.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
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
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/", 
 "searchserverurl":"https://s7search1.scene7.com/s7search/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

The following examples page illustrates more real-life use cases of responsive design embedding with unrestricted height:

[Live Demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

**Flexible size embedding with width and height defined**

In case of flexible-size embedding with width and height defined, the web page styling is different. That is, it provides both sizes to the " holder" `DIV` and centers it in the browser window. Also, the web page sets the size of the `HTML` and `BODY` element to 100%:

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
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
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
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/", 
 "searchserverurl":"https://s7search1.scene7.com/s7search/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Embedding Using Setter-based API**

Instead of using JSON-based initialization it is possible to use setter-based API and no-args constructor. With that API constructor does not take any parameters and configuration parameters is specified using `setContainerId()`, `setParam()`, and `setAsset()` API methods with separate JavaScript calls.

The following example shows fixed size embedding with setter-based API:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7ecatalogsearchviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer(); 
eCatalogSearchViewer.setContainerId("s7viewer"); 
eCatalogSearchViewer.setParam("serverurl", "https://s7d1.scene7.com/is/image/"); 
eCatalogSearchViewer.setParam("searchserverurl", "https://s7search1.scene7.com/s7search/"); 
eCatalogSearchViewer.setAsset("Viewers/Pluralist"); 
eCatalogSearchViewer.init(); 
</script> 
</body> 
</html>
```
