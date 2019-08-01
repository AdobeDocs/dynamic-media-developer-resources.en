---
description: Configuration attribute for Video360 Viewer.
seo-description: Configuration attribute for Video360 Viewer.
seo-title: Video360Player.ssl
solution: Experience Manager
title: Video360Player.ssl
topic: Dynamic media
uuid: 00c8295c-cc41-489c-a444-ba9189426a20
index: y
internal: n
snippet: y
---

# Video360Player.ssl{#video-player-ssl}

Configuration attribute for Video360 Viewer.

>[!NOTE]
>
>This configuration attribute only applies to AEM 6.2 with installation of [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

`[Video360Player.|<containerId>_video360Player.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|on</span> </p> </td> 
   <td colname="col2"> <p> Controls whether the video is delivered over a secure SSL connection (HTTPS) or an insecure connection(HTTP). </p> <p>When set to <span class="codeph"> auto</span> the video delivery protocol is inherited from the protocol of the embedding web page. If the web page is loaded over HTTPS, the video is also delivered over HTTPS, and vice versa. If the web page is on HTTP, the video is delivered over HTTP. </p> <p>When set to <span class="codeph"> on</span>, video delivery always occurs over a secure connection without regard to the web page protocol. </p> <p>Affects published video delivery only and is ignored for video preview in Author mode. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Default {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Example {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
ssl=on
```

<a id="section_5943AC73316749C68761FF7F74DA7547"></a>

See also [Secure Video Delivery](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-securevideodelivery.md#concept-13f66fdd4a52494aa516cd0f36fdac27). 
