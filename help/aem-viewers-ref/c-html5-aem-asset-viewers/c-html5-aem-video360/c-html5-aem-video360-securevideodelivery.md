---
description: null
seo-description: null
seo-title: HTTPS video delivery
solution: Experience Manager
title: HTTPS video delivery
topic: Dynamic media
uuid: 68984ba1-2802-496a-8ad0-ba46b59514ad
---

# HTTPS video delivery{#https-video-delivery}

>[!NOTE]
>
>HTTP Secure Video Delivery applies only to AEM 6.2 with the installation of [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

Provided that the viewer works in configuration as outlined at the beginning of this section, published video delivery can happen both in HTTPS (secure) and HTTP (insecure) modes. In a default configuration, the video delivery protocol strictly follows the delivery protocol of the embedding web page. However, it is possible to force HTTPS video delivery without regard to the protocol used by embedding the web page using the [Video360Player.ssl](r_html5_aem_video360_config_attrib_videoplayer_ssl.md#reference_C28E1B700977493EADAB5489458D7771) configuration attribute. (Note that video preview in Author mode is always delivered securely over HTTPS.)

Depending on the method of publishing Dynamic Media video that you use in AEM, the `Video360Player.ssl` configuration attribute is applied differently as demonstrated in the following:

* If you publish a Dynamic Media video with a URL, you append `Video360Player.ssl` to the URL. For example, to force secure video delivery, you append `&Video360Player.ssl=on` to the end of the following viewer URL example:

  ```
  https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/Video360Viewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&Video360Player.ssl=on
  ```

  See also [(AEM 6.2) Linking URLs to your Web Application](https://docs.adobe.com/content/docs/en/aem/6-2/author/assets/dynamic-media/delivering-dynamic-media-assets/linking-urls-to-yourwebapplication.html) or [(AEM 6.1) Linking URLs to your Web Application](https://docs.adobe.com/content/docs/en/aem/6-1/author/assets/dynamic-media/delivering-dynamic-media-assets/linking-urls-to-yourwebapplication.html) 

* If you publish a Dynamic Media video with embed code, you add `Video360Player.ssl` to the list of other viewer configuration parameters in the embed code snippet. For example, to force HTTPS video delivery, you append `&Video360Player.ssl=on` as in the following example:

  ```
  <style type="text/css"> 
   #s7video_div.s7video360viewer{ 
     width:100%;  
     height:auto; 
   } 
  </style> 
  <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js"></script> 
  <div id="s7video_div"></div> 
  <script type="text/javascript"> 
   var s7video360viewer = new s7viewers.Video360Viewer({ 
    "containerId" : "s7video_div", 
    "params" : {  
     "Video360Player.ssl" : "on", 
     "serverurl" : "https://adobedemo62-h.assetsadobe.com/is/image", 
     "contenturl" : "https://demos-pub.assetsadobe.com/",  
     "config" : "/etc/dam/presets/viewer/Video", 
     "config2": "/etc/dam/presets/analytics", 
     "videoserverurl": "https://gateway-na.assetsadobe.com/DMGateway/public/demoCo", 
     "posterimage": "/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4", 
     "asset" : "/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4" } 
   }).init(); 
  </script>
  ```

  See also [(AEM 6.2) Embedding the Video on a Web Page](https://docs.adobe.com/content/docs/en/aem/6-2/author/assets/dynamic-media/delivering-dynamic-media-assets/embed-code.html) or [(AEM 6.1) Embedding the Video on a Web Page](https://docs.adobe.com/content/docs/en/aem/6-1/author/assets/dynamic-media/delivering-dynamic-media-assets/embed-code.html).

