---
description: null
seo-description: null
seo-title: HTTPS video delivery
solution: Experience Manager
title: HTTPS video delivery
topic: Dynamic media
uuid: 7f8c1fe6-b464-4d80-9ffe-a36081825d49
index: y
internal: n
snippet: y
---

# HTTPS video delivery{#https-video-delivery}

>[!NOTE]
>
>Secure Video Delivery only applies to AEM 6.2 with the installation of [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

Provided that the viewer works in configuration as outlined at the beginning of this section, published video delivery can happen both in HTTPS (secure) and HTTP (insecure) modes. In a default configuration, the video delivery protocol strictly follows the delivery protocol of the embedding web page. However, it is possible to force HTTPS video delivery without regard to the protocol used by embedding the web page using the [VideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e) configuration attribute. (Note that video preview in Author mode is always delivered securely over HTTPS.)

Depending on the method of publishing Dynamic Media video that you use in AEM, the `VideoPlayer.ssl` configuration attribute is applied differently as demonstrated in the following:

* If you publish a Dynamic Media video with a URL, you append `VideoPlayer.ssl` to the URL. For example, to force secure video delivery, you append `&VideoPlayer.ssl=on` to the end of the following viewer URL example:

  ```
  https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/MixedMediaViewer.html?asset=%2Fcontent%2Fdam%2FGeometrixx-Outdoors-New-Launch%2Fbackpack%2Fbackpack_mixed_media&config=/etc/dam/presets/viewer/MixedMedia_light&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&VideoPlayer.ssl=on
  ```

  See also [(AEM 6.2) Linking URLs to your Web Application](https://docs.adobe.com/content/docs/en/aem/6-2/author/assets/dynamic-media/delivering-dynamic-media-assets/linking-urls-to-yourwebapplication.html) or [(AEM 6.1) Linking URLs to your Web Application](https://docs.adobe.com/content/docs/en/aem/6-1/author/assets/dynamic-media/delivering-dynamic-media-assets/linking-urls-to-yourwebapplication.html) 

* If you publish a Dynamic Media video with embed code, you add `VideoPlayer.ssl` to the list of other viewer configuration parameters in the embed code snippet. For example, to force HTTPS video delivery, you append `&VideoPlayer.ssl=on` as in the following example:

  ```
  <style type="text/css"> 
   #s7mixedmedia_div.s7mixedmediaviewer{ 
     width:100%;  
     height:auto; 
   } 
  </style> 
  <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/MixedMediaViewer.js"></script> 
  <div id="s7mixedmedia_div"></div> 
  <script type="text/javascript"> 
   var s7mixedmediaviewer = new s7viewers.MixedMediaViewer({ 
    "containerId" : "s7mixedmedia_div", 
    "params" : {  
     "VideoPlayer.ssl" : "on", 
     "serverurl" : "https://adobedemo62-h.assetsadobe.com/is/image", 
     "contenturl" : "https://demos-pub.assetsadobe.com/",  
     "config" : "/etc/dam/presets/viewer/MixedMedia_light", 
     "config2": "/etc/dam/presets/analytics", 
     "videoserverurl": "https://gateway-na.assetsadobe.com/DMGateway/public/demoCo", 
     "asset" : "/content/dam/Geometrixx-Outdoors-New-Launch/backpack/backpack_mixed_media" } 
   }).init(); 
  </script>
  ```

  See also [(AEM 6.2) Embedding the Video on a Web Page](https://docs.adobe.com/content/docs/en/aem/6-2/author/assets/dynamic-media/delivering-dynamic-media-assets/embed-code.html) or [(AEM 6.1) Embedding the Video on a Web Page](https://docs.adobe.com/content/docs/en/aem/6-1/author/assets/dynamic-media/delivering-dynamic-media-assets/embed-code.html).

