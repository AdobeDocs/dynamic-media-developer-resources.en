---
title: Hotspot and Image maps support
description: Hotspot and Image maps support
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: b441e241-809e-47cf-a309-57283bd0532b
---
# Hotspot and Image maps support{#hotspot-and-image-maps-support}

The viewer supports the rendering of hotspot icons and image map regions on top of the main view. The appearance of hotspot icons and regions is controlled through CSS as described in the customize Hotspots and Image maps section.

See [Hotspots and Image maps](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Hotspots and regions can either activate a Quickview feature on the hosting web page by triggering a JavaScript callback or redirect a user to an external web page.

## Quickview hotspots {#section-cda48fc9730142d0bb3326bac7df3271}

These types of hotspots or image maps should be authored using the "Quickview" action type in Dynamic Media, of Adobe Experience Manager. When a user activates such a hotspot or image map, the viewer runs the `quickViewActivate` JavaScript callback and passes the hotspot or image map data to it. It is expected that the embedding web page listens for this callback. When it triggers the page, it opens its own Quickview implementation.

## Redirect to external web page {#section-ef820c71251e4215800bb99c0c9ebe16}

Hotspots or image maps authored for the action type "Quickview" in Dynamic Media of Experience Manager redirects the user to an external URL. Depending on settings made during authoring, the URL opens in a new browser tab, in the same window, or in the named browser window.
