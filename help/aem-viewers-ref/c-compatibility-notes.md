---
description: Compatibility notes for operating systems, browsers, and mobile devices.


solution: Experience Manager
title: Compatibility notes

feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,Business Practitioner
---

# Compatibility notes{#compatibility-notes}

<!-- Updated January 13,2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Compatibility notes for operating systems, browsers, and mobile devices.

## Blackberry {#section-0c465ac3775d47fd838e2695a00abc45}

* Incompatibility with older Adaptive Video Sets. You may need to re-upload Adaptive Video Sets to allow playback.

## General {#section-7b9a9fcba85148d1802b7b3016b48e02}

* Browser side scaling may cause UI and images to become blurry as user zooms into page. UI formatting may also display incorrectly depending upon zoom. This will carry over to full screen.
* Due to the size limitation on mobile devices the Mixed Media Viewer uses slide gesture to swap frames in embedded image sets instead of tapping the embedded swatches component. Component is there as a visual indicator.
* In Internet Explorer browsers and some touch devices, full-screen mode does not occupy the entire device screen. Instead, it resizes the application to the size of the browser window.
* Close button does not work under iOS 8.0 and iOS 8.1 but works under iOS 8.2.

## Galaxy SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* Memory leak seen with Zoom and eCatalog viewers. Repeated navigation through frames may cause browser to crash.
* Double-tapping on a viewer may cause the entire page to zoom instead of just the viewer with browser-side scaling enabled.

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* Device detected as tablet in portrait mode with Full Screen checked in browser settings.

## Galaxy Nexus {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* Double-tapping on a viewer may cause the entire page to zoom instead of just the viewer, with browser-side scaling enabled.

## Galaxy Nexus 10 and Galaxy Tablet {#section-ef52bd1249fe4f358c11838f7a557a00}

* eCatalog shows incorrect page spread with portrait and landscape orientations.

## HTC Mobile Devices {#section-dc42c80414c842e488738fc157c55b01}

* Inability to disable native pinch-zoom is a "feature" of HTC UI wrapper (HTC Sense). This feature can cause an entire page to zoom when using "pinch to zoom" gesture on the viewer. Use a double-tap gesture instead.
* Image map icons may overlap if image maps are small and close together.

## HTML5 Video Viewer {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` modifier is only supported with software HLS and flash HDS playback. It does not work when playback is using the native player.
* OGG and WebM progressive playback not supported.
* Browser scaling may cause the video player to display at an incorrect size (include Windows OS control panel Display settings).
* Video seek using HLS streaming on Safari may be inconsistent.

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* Quirks mode is not supported.
* Compatibility mode is not supported.
* Internet Explorer on mobile is not supported.

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* Large eCatalogs may cause the browser to crash on iPad 2.

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1 or later: Internet Plug-in settings may prevent Flash video playback.
* Video seek using HLS streaming on Safari may be inconsistent.
* Unable to seek to end of video on Safari 6 using HLS streaming.
