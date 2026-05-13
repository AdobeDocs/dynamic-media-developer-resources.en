---
description: An image server proxy can be used to resize images for Japanese phones.
solution: Experience Manager
title: Image server proxy
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0389a4af-a412-42eb-b7b4-716e47d623a0
TQID: 'https://experienceleague.adobe.com/wJ6wQsus1QmfFbZ4FCM1nAmPdWacySEWaV9vfAA1fyg'
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
  <td class="stentry"> <p>Specifies the percentage of the device's Memory Limit Embedded Media property to limit the response size to. This only applies to jpg responses. The quality of the image is lowered until the response size is within the specified percentage. </p></td> 
 </tr> 
</table>

## Embedded image memory limit {#section-52f7c69ed8a341ceabf92ceee19b0f36}

If the device has a limit on the size of images that can be embedded on a web page, image size is restricted to that size as long as the response format is jpg. The proxy limits responses to 500MB if the device does not have any limit.

## Backend processing {#section-bdf7c294b6824de9969c97fc1f8aa6d3}

The proxy downloads, verifies, and loads the Device Atlas data file once a day. The verification pulls out different properties for different devices and compares them with expected values before accepting the new data.
