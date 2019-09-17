---
description: The eCatalog Search Viewer supports the rendering of image map icons above the main view.
seo-description: The eCatalog Search Viewer supports the rendering of image map icons above the main view.
seo-title: Image map support
solution: Experience Manager
title: Image map support
topic: Dynamic media
uuid: 22ba8168-b384-4eda-a147-ce8172cfed11
---

# Image map support{#image-map-support}

The eCatalog Search Viewer supports the rendering of image map icons above the main view.

The appearance of map icons is controlled through CSS as described in [Image map effect](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289).

Image maps perform one of the following three actions: redirect to an external web page, Info panel pop-up activation, and internal hyperlinks.

## Redirect to an external web page {#section-32ebe3c3a7f74892a428c5d48801de4d}

The `href` attribute of the image map has a URL to the external resource, either specified explicitly, or wrapped into one of the supported JavaScript template functions: `loadProduct()`, `loadProductCW()`, and `loadProductPW()`.

The following is an example of a simple URL redirect:

`href=http://www.adobe.com`

In this example, the same URL is wrapped with the `loadProduct()` function:

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Be aware that when you add the JavaScript code into the `HREF` attribute of your image map, the code is run on the client’s computer. Therefore, make sure that the JavaScript code is secure.

## Info Panel Popup activation {#section-7aa036420af646d1ad8cdc388add0b57}

To work with Info panels, an image map has the `ROLLOVER_KEY` attribute set. Also, set the `href` attribute at the same time, otherwise the external URL processing interferes with the Info panel pop-up activation.

Finally, be sure that the viewer configuration includes the appropriate values for `InfoPanelPopup.template` and, optionally, `InfoPanelPopup.infoServerUrl` parameters.

>[!NOTE]
>
>Be aware that when you configure Info Panel Popup, the HTML code and JavaScript code passed to the Info Panel runs on the client's computer. Therefore, make sure that such HTML code and JavaScript code are secure.

## Internal hyperlinks {#section-6afa4fb2fe564c429e0201f019a95849}

Clicking on an image map performs an internal page swap inside the viewer. To use that feature, an `href` attribute in the image map has the following special format:

` href=target: *`idx`*`

where ` *`idx`*` is a zero-based index of the catalog spread.

The following is an example of an `href` attribute for an image map that points to the 3D spread in the eCatalog:

`href=target:2` 
