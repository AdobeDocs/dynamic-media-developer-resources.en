---
description: Carousel Viewer is a viewer that displays a carousel of non-zoomable banner images with clickable hotspots or regions. The purpose of this viewer is to implement a "shoppable carousel" experience where users can select a hotspot or a region over the banner image and get redirected to a Quickview or product detail page on the customer's website. It is designed to work on desktops and mobile devices.


solution: Experience Manager
title: Carousel

feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
---

# Carousel{#carousel}

Carousel Viewer is a viewer that displays a carousel of non-zoomable banner images with clickable hotspots or regions. The purpose of this viewer is to implement a "shoppable carousel" experience where users can select a hotspot or a region over the banner image and get redirected to a Quickview or product detail page on the customer's website. It is designed to work on desktops and mobile devices.

>[!NOTE]
>
>Images that use Image Rendering or User-Generated Content (UGC) are not supported by this viewer.

Viewer type is 511.

## Demo URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/CarouselViewerDemo.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/CarouselViewerDemo.html)

## System Requirements {#section-b7270cc4290043399681dc504f043609}

See [System requirements](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Using Carousel Viewer {#section-e6c68406ecdc4de781df182bbd8088b4}

Carousel Viewer represents a main JavaScript file and a set of helper files (a single JavaScript include with all Viewer SDK components used by this particular viewer, assets, CSS) downloaded by the viewer in runtime.

Carousel Viewer can be used both in pop-up mode using a production-ready HTML page provided with IS Viewers, or in embedded mode where it is integrated into the target web page using documented API.

Configuration and skinning are similar to that of the other viewers described in this Help. All skinning is achieved by way of custom CSS.

See [Command reference common to all viewers - Configuration attributes](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) and [Command reference common to all Viewers - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interacting with Carousel Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

Navigating through the carousel set is done using a horizontal swipe over the main view or with two arrow buttons available on the desktop device. Set indicator dots show the current position within the set.

The viewer can render hotspots or regions on top of the banner image to indicate the interactive area on the product.

Clicking or tapping on a hotspot or a region triggers an action associated with it during the author time. The action may be redirected to a different page on the web site, or it can pass product information back to the web page logic, which in turn can trigger a Quickview with related product content.

The viewer is fully keyboard accessible.

See [Keyboard accessibility and navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Embedding Carousel Viewer {#section-6bb5d3c502544ad18a58eafe12a13435}

**About pop-up mode**

In pop-up mode, the viewer is opened in a separate web browser window or tab. It takes the entire browser window area and adjusts in case the browser is resized, or a mobile device's orientation is changed.

Pop-up mode is the most common for mobile devices. The web page loads the viewer using `window.open()` JavaScript call, properly configured `A` HTML element, or any other suitable method.

It is recommended that you use an out-of-the-box HTML page for pop-up operation mode. In this case, it is called `CarouselViewer.html` and is located within the `html5/` subfolder of your standard IS-Viewers deployment:

`<s7viewers_root>/html5/CarouselViewer.html`

You can achieve visual customization by applying custom CSS.

The following is an example of HTML code that opens the viewer in a new window:

```
<a href="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/CarouselViewer.html?asset=/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner&serverurl=https://adobedemo62-h.assetsadobe.com/is/image" target="_blank">Open popup viewer</a>
```

**About fixed size embedding mode and responsive design embedding mode**

In the embedded mode, the viewer is added to the existing web page. This web page may already have some customer content not related to the viewer. The viewer normally occupies only a part of a web page's real estate.

The primary use cases are web pages oriented for desktops or tablet devices, and responsive designed pages that adjust layout automatically depending on the device type.

Fixed size embedding is used when the viewer does not change its size after initial load. This is the best choice for web pages that have a static layout.

Responsive design embedding assumes that the viewer may need to resize at runtime in response to the size change of its container `DIV`. The most common use case is adding a viewer to a web page that uses a flexible page layout.

In responsive design embedding mode, the viewer behaves differently depending on the way web page sizes its container `DIV`. If the web page sets only the width of the container `DIV`, leaving its height unrestricted, the viewer automatically chooses its height according to the aspect ratio of the asset used. This functionality ensures that the asset fits perfectly into the view without any padding on the sides. This use case is the most common for web pages using responsive web design layout frameworks like Bootstrap, Foundation, and so on.

Otherwise, if the web page sets both the width and the height for the viewer's container `DIV`, the viewer fills just that area. It also follows the size that the web page layout provides. A good example is embedding the viewer into a modal overlay, where the overlay is sized according to web browser window size.

**Fixed size embedding**

You add the viewer to a web page by doing the following:

1. Adding the viewer JavaScript file to your web page. 
1. Defining the container `DIV`. 
1. Setting the viewer size. 
1. Creating and initializing the viewer.

1. Adding the viewer JavaScript file to your web page.

   Creating a viewer requires that you add a script tag in the HTML head. Before you can use the viewer API, be sure that you include [!DNL CarouselViewer.js]. The [!DNL CarouselViewer.js] file is located under the [!DNL html5/js/] subfolder of your standard IS-Viewers deployment:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js]

   You can use a relative path if the viewer is deployed on one of the Adobe Dynamic Media Classic servers and it is served from the same domain. Otherwise, you specify a full path to one of Adobe Dynamic Media Classic servers that have the IS-Viewers installed.

   The relative path looks like the following:

   ```
   <script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script>
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

   The following is an example of a defined placeholder `DIV` element:

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Setting the viewer size

   You can set the static size for the viewer by either declaring it for `.s7carouselviewer` top-level CSS class in absolute units, or by using `stagesize` modifier.

   You can put sizing in CSS directly on the HTML page, or in a custom viewer CSS file, which is then later assigned to a viewer preset record in AEM Assets - on-demand, or passed explicitly using the `style` command.

   See [Customizing Carousel Viewer](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/c-html5-aem-carousel-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) for more information about styling the viewer with CSS.

   The following is an example of defining a static viewer size in the HTML page:

   ```
   #s7viewer.s7carouselviewer { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   You can pass explicitly the `stagesize` modifier with the viewer initialization code with `params` collection or as an API call as described in the Command Reference section, like this:

   ```
   carouselViewer.setParam("stagesize", "1174,500");
   ```

   A CSS-based approach is recommended and is used in this example. 

1. Creating and initializing the viewer.

   When you have completed the steps above, you create an instance of `s7viewers.CarouselViewer` class, pass all configuration information to its constructor, and call `init()` method on a viewer instance. Configuration information is passed to the constructor as a JSON object. At minimum, this object should have `containerId` field which holds the name of viewer container ID and nested `params` JSON object with configuration parameters supported by the viewer. In this case, the `params` object must have at least the Image Serving URL passed as `serverUrl` property, and the initial asset as `asset` parameter. The JSON-based initialization API lets you create and start the viewer with a single line of code.

   It is important to have the viewer container added to the DOM so that the viewer code can find the container element by its ID. Some browsers delay building DOM until the end of the web page. For maximum compatibility, call the `init()` method just before the closing `BODY` tag, or on the body `onload()` event.

   At the same time, the container element should not necessarily be part of the web page layout just yet. For example, it may be hidden using `display:none` style assigned to it. In this case, the viewer delays its initialization process until the moment when the web page brings the container element back to the layout. When this happens, the viewer load automatically resumes.

   The following is an example of creating a viewer instance, passing minimum necessary configuration options to the constructor and calling the `init()` method. The example assumes `carouselViewer` is the viewer instance; `s7viewer` is the name of placeholder `DIV`; `https://adobedemo62-h.assetsadobe.com/is/image` is the Image Serving URL, and `/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner` is the asset:

   ```
   <script type="text/javascript"> 
   var carouselViewer = new s7viewers.CarouselViewer ({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
    "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script>
   ```

   The following code is a complete example of a trivial web page that embeds the Carousel Viewer with a fixed size:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7carouselviewer { 
    width: 1174px; 
    height: 500px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var carouselViewer = new s7viewers.CarouselViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
    "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Responsive design embedding with unrestricted height**

With responsive design embedding, the web page normally has some kind of flexible layout in place that dictates the runtime size of the viewer's container `DIV`. For the following example, assume that the web page allows the viewer's container `DIV` to take 40% of the web browser window size. And, its height is left unrestricted. The web page HTML code would look like the following:

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

Adding the viewer to such a page is similar to the steps for fixed size embedding. The only difference is that you do not need to explicitly define the viewer size.

1. Adding the viewer JavaScript file to your web page. 
1. Defining the container `DIV`. 
1. Creating and initializing the viewer.

All the steps above are the same as with the fixed size embedding. Add the container `DIV` to the existing `"holder"` `DIV`. The following code is a complete example. Notice how the viewer size changes when the browser is resized, and how the viewer aspect ratio matches the asset.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
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
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html>
```

The following examples page illustrates more real-life uses of responsive design embedding with unrestricted height:

[https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/CarouselViewer-responsive-unrestricted-height.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/CarouselViewer-responsive-unrestricted-height.html)

**Flexible size Embedding with Width and Height Defined**

In case of flexible-size embedding with width and height defined, the web page styling is different. It provides both sizes to the `"holder"` DIV and center it in the browser window. Also, the web page sets the size of the `HTML` and `BODY` element to 100 percent.

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
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
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
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
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
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7carouselviewer { 
 width: 1174px; 
 height: 500px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var carouselViewer = new s7viewers.CarouselViewer(); 
carouselViewer.setContainerId("s7viewer"); 
carouselViewer.setParam("serverurl", "https://adobedemo62-h.assetsadobe.com/is/image"); 
carouselViewer.setAsset("/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner"); 
carouselViewer.init(); 
</script> 
</body> 
</html>
```

