---
description: An image server proxy can be used to resize images for Japanese phones.
solution: Experience Manager
title: Image server proxy
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# Image server proxy{#image-server-proxy}

An image server proxy can be used to resize images for Japanese phones.

## URL format {#section-2e8c40b0547c4f99874cdf502b338940}

The url format for the IS proxy is very similar to regular IS requests. Any IS modifiers passed to the proxy is passed through to the Image Server. You can find info on the IS modifiers in the [HTTP Protocol Reference](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-introduction/c-introduction.md#concept-dbbd5241bc6248ad9b9d7f6c635c311e).

`http://<server>/is-proxy/image/<company><asset>?<modifiers>`

`http://<server>/is-proxy/image/sample/chair?qlt=75`

## Proxy-specific modifier list {#section-1bff28f9cf5b4e04a31308b06176ee5f}

<table id="simpletable_40C1DFB183B54A79BCF65D51ED480CE0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> widpercent = &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Specifies the percentage of the device's usable width to use as the image width. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> heipercent = &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Specifies the percentage of the device's usable height to use as the image height. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> sizepercent = &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Specifies the percentage of the device's Memory Limit Embedded Media property to limit the response size to. This will only apply to jpg responses. The quality of the image will be lowered until the response size is within the specified percentage. </p></td> 
 </tr> 
</table>

## Embedded image memory limit {#section-52f7c69ed8a341ceabf92ceee19b0f36}

If the device has a limit on the size of images that can be embedded on a web page, image size is restricted to that size as long as the response format is jpg. The proxy limits responses to 500MB if the device does not have any limit.

## Backend processing {#section-bdf7c294b6824de9969c97fc1f8aa6d3}

The proxy downloads, verifies, and loads the Device Atlas data file once a day. The verification pulls out different properties for different devices and compares them with expected values before accepting the new data. 
