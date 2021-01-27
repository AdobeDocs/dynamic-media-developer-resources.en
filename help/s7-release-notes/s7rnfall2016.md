---
description: The latest release notes for Adobe Scene7 Fall 2016 release–part of the Adobe Experience Manager solution in the Adobe Marketing Cloud.
solution: Experience Manager
title: Scene7 Fall 2016 Release
topic: Dynamic Media
---

# Scene7 Fall 2016 Release{#scene-fall-release}

The latest release notes for Adobe Scene7 Fall 2016 release–part of the Adobe Experience Manager solution in the Adobe Marketing Cloud.

## Scene7 Fall 2016 Release {#topic-791cdf80f91e457fbb63bfedf79f5a94}

The latest release notes for [!DNL Adobe Scene7] Fall 2016 release-part of the [!DNL Adobe Experience Manager] solution in the [!DNL Adobe Marketing Cloud].

* [General](s7rnfall2016.md#section-52afeb72ecb34c1585ea67a5051825a2) 
* [Scene7](s7rnfall2016.md#section-24487cb493444d808fb7193f0a00cdd4) 
* [Viewers (Image Serving 5.5.3)](s7rnfall2016.md#section-1d59bcd5825d487b80b59a6d1a08ed30) 
* [Viewers (Image Serving 5.5.2)](s7rnfall2016.md#section-9932c988cfee45749594af481dfc6476) 
* [Viewers (Image Serving 5.5.1)](s7rnfall2016.md#section-833ab92c91c941d2bfdc27f233f582ad) 
* [HTML5 Viewer SDK 3.0.1](s7rnfall2016.md#section-30e2392859c442d1aab2766d0f1d1580) 
* [Dynamic Media Classic Image Serving 6.3.2 and Image Rendering 6.3.2](s7rnfall2016.md#section-19a3e96f52c74757bcdea0f8a11001f2)

## General {#section-52afeb72ecb34c1585ea67a5051825a2}

Adobe is excited to announce the availability of HTTP/2 delivery of content with the overall benefit of improved performance.

See [HTTP2 Delivery of Content FAQ](https://docs.adobe.com/content/docs/en/aem/6-2/administer/integration/marketing-cloud/scene7/http2faq.html).

## Scene7 Publishing System {#section-24487cb493444d808fb7193f0a00cdd4}

For complete documentation, see [https://docs.adobe.com/content/help/en/dynamic-media-classic/using/home.html](https://docs.adobe.com/content/help/en/dynamic-media-classic/using/home.html)

**New features, enhancements, and bug fixes**

* Removed video recut feature from [!DNL Adobe Scene7 Publishing System] user interface. 
* Added authentication to all Scene7 servlets where necessary and possible. 
* Bug fix involving the List View in the Trash Can. 
* Removed **Create Dynamic Media Classic (Scene7) Admin** user feature from User Management because of security concerns. 
* FTP WebAdmin now supports OKTA authentication. 
* Removed the feature of the default password that got created for new Media Portal users. 
* Bug fix involving the temporary password that was generated when a new user was added. The password did not fulfill necessary password requirements. 
* Resolved issues of WebAdmin root disk full. 
* Bug fix involving the disabling of a user not being reflected immediately in the user interface. 
* Bug fix involving the deletion of a user which did not let you re-create the user later. 
* Bug fix involving the Welcome email sent to new Scene7 users that did not include authentication to control certain settings. 
* Bug fix involving the failure to retrieve an FTP folder list if any folder had special characters in its name. 
* Configure OKTA service providers for Scene7 environments. 
* Added support for Marketing Cloud Org ID for Viewer Analytics. 
* Implemented Scene7 SAML consumer.

## Viewers (Image Serving 5.5.3) {#section-1d59bcd5825d487b80b59a6d1a08ed30}

For complete documentation, see [Viewers Reference Guide](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/library/home.html).

**Bug fixes for Image Serving 5.5.3**

* Compatibility with RequireJS and DOJO libraries.

  Consolidated SDK JS caching during viewer deployment.

## Viewers (Image Serving 5.5.2) {#section-9932c988cfee45749594af481dfc6476}

For complete documentation, see [Viewers Reference Guide](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/library/home.html).

**Bug fixes for Image Serving 5.5.2**

* Video failed to play in Internet Explorer 11 on Windows 7. 
* `initialframe` was not affecting portrait mode on mobile devices for HTML5 eCatalog.

## Viewers (Image Serving 5.5.1) {#section-833ab92c91c941d2bfdc27f233f582ad}

For complete documentation, see [Viewers Reference Guide](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/library/home.html).

**New features, enhancements, and bug fixes for Image Serving 5.5.1**

* HTML5 eCatalog viewer with search feature. 
* Added HLS streaming video playback as a default video delivery method for majority of desktop systems. Flash-based HDS video streaming is still available as an alternative playback option. 
* Added support for devices with both mouse and touch input running Chrome browser. 
* Added Marketing Cloud Org ID support to the Analytics integration. 
* Update AppMeasurement JavaScript library to version 1.6.1. 
* Added support for right-to-left orientation in the eCatalog viewer. 
* Fixed issue where `tip=0,-1,0` caused an out-of-range error.

**Compatibility notes**

* Blackberry

  * Incompatibility with older AVS sets. Clients may need to re-upload AVS sets to allow playback.

* General

  * Browser side scaling may cause UI and images to become blurry as user zooms into page. UI formatting may also display incorrectly depending upon zoom. This will carry over to full screen. 
  * Due to size limitation on mobile devices the Mixed Media Viewer uses slide gesture to swap frames in embedded image sets instead of tapping the embedded swatches component. The component is there as a visual indicator. 
  * In Internet Explorer browsers and some touch devices, full screen mode does not occupy entire device screen. Instead, it resizes application to the size of the browser window. 
  * The Close button does not work iOS 8.0 and 8.1 but no longer occurs in iOS 8.2

* Galaxy SIII

  * Memory leak seen with Zoom and eCatalog HTML5 viewers. Repeated navigation through frames may cause browser to crash. 
  * Double tap on viewer may cause whole page to zoom instead of just viewer with browser side scaling enabled.

* Galaxy S4

  * Device detected as tablet in portrait mode with Full Screen checked in browser settings.

* Galaxy Nexus

  * Double tap on viewer may cause whole page to zoom instead of just viewer with browser side scaling enabled.

* Galaxy Nexus 10 and Galaxy Tablet

  * eCatalog showing incorrect page spread with portrait and landscape orientations.

* HTC Mobile Devices

  * HTC mobile devices our findings show that inability to disable native pinch-zoom is a "feature" of HTC UI wrapper (HTC Sense). This may cause whole page to zoom when using "pinch to zoom" gesture on viewer. Suggest using double-tap instead. 
  * Image map icons may overlap if image maps are small and close together.

* HTML5 Video

  * Internet Explorer 9: custom poster images do not display. 
  * `IntialBitRate` modifier is only supported with software HLS and Flash HDS playback. It does not work when playback is using the native player. 
  * OGG and WebM progressive playback not supported at this time. 
  * Browser scaling can cause the video player to display at an incorrect size (include Windows OS control panel Display settings) 
  * Video seek using HLS streaming on Safari may be inconsistent.

* Internet Explorer

  * Quirks mode is not supported at this time. 
  * Compatibility mode is not supported at this time. 
  * Internet Explorer on mobile is not supported at this time.

* iOS

  * Large eCatalogs may cause browser crash on iPad 2. 
  * iPhone 6+ phones are detected as tablets by the viewers.

* Safari

  * Safari 6.1 or later: Internet Plug-ins settings may prevent Flash video playback. 
  * Video "seek" using HLS streaming on Safari may be inconsistent. 
  * Unable to seek to end of video on Safari 6 using HLS streaming.

**Known issues and restrictions**

* The Image Serving modifiers from `iscommands` are not added to the `req=set` request by design. Modifiers that only affect image display work fine. Modifiers affecting size must be used in a complex asset. For example,

  `https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset= {Scene7SharedAssets/Backpack_B?extendn=0.5%252C0.5%252C0.5%252C0.5}` 

* [Flyout] IE9 sometimes remains on screen after mouse off. 
* Browser scaling leads to wrong resizing. 
* iPad 2: Big eCatalog asset will crash Safari on iOS. 
* All Viewers

  * Watermarks, obfuscation, and locking are not supported. 
  * Image presets are not supported. 
  * Adding or removing viewer from the DOM using `display:none` CSS or by dynamically detaching it from the parent node is not supported at this time.

* HTML5 All Viewers

  * Embedding viewer in table may result in incorrect sizing or placement of viewer in non-native fullscreen mode. Suggest using DIVs instead. 
  * Parameters with explicit instance names in the code require instance names in the URL as well to be overwritten (for example, `zoomView.iconfeffect=0`). 
  * Image Serving command crop is not supported at this time. 
  * The Close button works only if the viewer is open in the child window. 
  * The `iscommands` modifier does not support Image Serving modifiers that affect image size.

* HTML5 eCatalog

  * Navigating to other HTML page and returning occasionally causes viewer to reset back to first page. 
  * Page layout occasionally displays incorrectly after rotating iOS device. Zooming into page corrects layout. 
  * Internal links only to leftmost page in multi-page spreads. Affects mobile devices in portrait mode. 
  * InitalFrame links only to leftmost page in multi-page spreads. Affects mobile devices in portrait mode. 
  * Due to browser limitations, print feature is not available in IE9.

* HTML5 MixedMedia

  * Soundtrack play is currently not supported.

* HTML5 Social

  * To render thumbnails properly in outgoing email the `serverurl` modifier must have an absolute URL.

* HTML5 Video

  * The poster image may encounter "max size" error. Company may need to increase limit setting for Image Serving Publish. 
  * Video captions require a company ruleset if hosting the HTML page is served from an external server (not a Scene7 server). Contact Adobe Support for assistance. 
  * Analytics tracking may report incorrect play percentage due to buffering 
  * Black frame instead of poster image may show on iPad or Android devices. 
  * Black frame may flash on screen during viewer load on iPad or Android devices. 
  * Black borders are shown on side of VideoPlayer component when background is set to white/transparent on iPad devices. 
  * Last frame of video may be distorted on iPad using iOS 7. 
  * Occasional macroblocking may occur during video seek in HLS streaming mode in Chrome, Firefox and Internet Explorer browsers. 
    * Poster image may not show in Microsoft Edge browser for the first time visitor. 
    * Poster image may hide after video load in Internet Explorer 9 when progressive playback is used.

## Scene7 HTML5 Viewer SDK 3.0.2 {#section-30e2392859c442d1aab2766d0f1d1580}

The User Guide is located in the Adobe HTML5 Viewer SDK folder of the client install. Component API documentation is found in the docs subfolder of the client install.

**Bug fixes for 3.0.2**

* VideoPlayer - Video failed to play in Internet Explorer 11 on Windows 7 
* TableOfContents -  `initialframe` did not affect portrait mode on mobile devices for HTML5 eCatalog viewer.

**New features, enhancements, and bug fixes for 3.0.1**

* General

  * Added HLS streaming video playback as a default video delivery method for majority of desktop systems. Flash-based HDS video streaming is still available as an alternative playback option. 
  * Added SearchManager, SearchPanel, SearchEffect, and SearchButton components to support new Search feature in eCatalog viewers. 
  * Added support for devices with both mouse and touch input running on Chrome browser. 
  * Refactored Android version detection to support future versions of the OS 
  * Add support for right-to-left orientation in eCatalog-specific SDK components.

* ControlBar

  * Added optional scrolling for ControlBar content in case it does not fit into the available width.

* FlyoutzoomView

  * Fixed case where `tip=0,-1,0` caused an out-of-range error.

**Compatibility notes**

* Android 4.x

  * To disable the default, blue highlight the following CSS rule needs to be added for component:

      `-webkit-tap-highlight-color: rgba(0,0,0,0);`

* Blackberry

  * Video play may cease when changing bit rate streams in AVS sets.

* Chrome

  * Any API calls which forces component rebuild may be ignored due to Chrome's internal caching.

* Galaxy SIII

  * Viewer sometimes fails to load into full screen. 
  * Pageview suffers from a memory leak on device at this time. 
  * Double tap gesture zooms viewer and page when browser side scaling is active.

* Galaxy Nexus

  * Artifacts displaying over some view components. 
  * Double tap gesture zooms viewer and page when browser side scaling is active.

* iPad 3

  * The iPad 3 has a native resolution of 2048x1536. This can cause display problems if the company's IS publish, image size limit set lower than that.

* iPhone4

  * Iconeffect replay icon replaced with play icon after scrolling page.

* Internet Explorer

  * On IE 10 and older full screen mode does not occupy entire screen, instead it just resizes application to the size of the browser window. 
  * Quirks render mode is not supported. 
  * Internet Explorer on mobile is not supported at this time. 
  * Util.js may fail to load if included asynchronously. 
  * IconEffect icon blocks click events on SpinView and ZoomView components.

* Native device video players

  * Layering UI components over VideoPlayer are not supported when VideoPlayer is used to call the device's native player. 
  * Video playback in native mode is inconsistent on Safari 6. 
  * Native playback replaces replay icon with play icon after scrolling page.

* Touch devices

  * Full screen mode does not occupy entire device screen, instead it just resizes application to the size of the browser window. 
  * Custom cursors do not work on touch devices. 
  * Page scaling on touch devices is not supported at this time. Embedding HTML5 viewers require viewport meta tag with appropriate settings.

* Xoom

  * Double tap gesture zooms viewer and page when browser side scaling is active.

**Known issues and restrictions**

* All components

  * In versions 2.7.2 and earlier some components were added to the DOM using `insertBefore()` API. As a result, such components would put themselves in the bottom of the stacking order, no matter when component instance is created relative to other components. With the 2.8.1 release all components are using `appendChild()` API now, which means that the component stacking order would match the order of instance creation. 

  * Using `iscommand` modifier to set image alpha channel format is not supported. Use component `FMT` parameter instead. 
  * CSS transform property is not supported at this time.

* Touch devices

  * Pinch gesture on touch devices does not generate a zoom event

* Container

  * Border, padding and margins on the container is not supported. Adobe suggests adding style elements to parent DIV. 
  * Need to explicitly set the container size or the components may be sized correctly.

* Print component

  * Due to browser limitations, in Internet Explorer 9, the print component may not scale the content properly on the paper.

* IconEffect component

  * IconEffect generates a script error on Internet Explorer if `autohide` is disabled (set to `0`).

* ImageMapEffect component

  * Delay with repositioning icon when panning image on view component.

* MediaSet component

  * Inline assets request same encoding as on the URL.

* NavigationView component

  * Currently the component does not support resize.

* PageScrubber component

  * On iPhone 5, when the PageScrubber bubble is set to text, it is displaying artifacts when sliding the button along the track. Using `-webkit-background-clip: content;` in the style works around the issue.

* SpinView component

  * SpinView sometimes appears to freeze after swipe gesture and rotating the device while image is spinning.

* Swatches component

  * When selecting an out of bounds swatch, 2 highlights are shown. 
  * Auto scrolling with `selectSwatch()` method working incorrectly.

* VideoPlayer

  * Video frame not updated if seek is set to 100 percent with the fallback set to auto. 
  * Occasional macro blocking may occur during video seek in HLS streaming mode in Chrome, Firefox and Internet Explorer browsers. 
  * Poster image may not show in Microsoft Edge browser for the first time visitor. 
  * Poster image may hide after video load in Internet Explorer 9 when progressive playback is used.

## Dynamic Media Image Serving 6.3.2 and Image Rendering 6.3.2 {#section-19a3e96f52c74757bcdea0f8a11001f2}

* IC utility - `downsample2x2` flag is no longer supported. This flag was a poor quality 2x2 downsampler that is no longer used by IPS. 
* CORS header - Currently, the CORS header is configured for `/is/content/` requests.

