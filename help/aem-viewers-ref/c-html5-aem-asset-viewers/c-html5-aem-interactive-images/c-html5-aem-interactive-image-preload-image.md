---
title: Preload image
description: Preload image is a static asset preview image which loads right after calling init() method and shows while Viewer SDK libraries, asset, and preset information is downloaded. The purpose of the preload image is to visually improve viewer load time and present content to the user quickly.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 54bea5fc-916c-4a58-bc06-b726884d488a
TQID: 'https://experienceleague.adobe.com/GlTbkyDeUNGf4gjmEEGbh1NaQ-nOgPZLtrz9kH4eK7o'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# Preload image{#preload-image}

Preload image is a static asset preview image which loads right after calling init() method and shows while Viewer SDK libraries, asset, and preset information is downloaded. The purpose of the preload image is to visually improve viewer load time and present content to the user quickly.

Preload image works well for the most common viewer embedding method, which is responsive embedding with unrestricted height. See the heading [Responsive design embedding with unrestricted height](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

The feature, however, has certain limitations when other embedding methods or specific configuration options are used. Preload image may fail to render properly in following cases:

* When the viewer is fixed in size and the size is defined either using `stagesize` configuration attribute inside the viewer preset record. Or, using the external viewer CSS file for the top-level viewer container element.
* When using the flexible size embedding with width and height defined method of viewer embedding. See the heading [Flexible size embedding with width and height defined](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Disable preload image feature using the `preloadImage` configuration attribute if you are using the viewer in one of the operation modes listed above.

Also, preload image is not used-even if enabled in the configuration-if the viewer is embedded into the DOM element is hidden using `display:none` CSS setting or detached from the DOM tree.
