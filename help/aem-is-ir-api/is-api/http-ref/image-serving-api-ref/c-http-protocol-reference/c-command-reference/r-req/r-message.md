---
description: Client message. Provides a mechanism for clients to insert short text messages into the server log.
seo-description: Client message. Provides a mechanism for clients to insert short text messages into the server log.
seo-title: message
solution: Experience Manager
title: message
topic: Scene7 Image Serving - Image Rendering API
uuid: 38d6d0e7-55cf-43ea-85b7-8f4aade4208a
---

# message{#message}

Client message. Provides a mechanism for clients to insert short text messages into the server log.

 `req=message&message= *`string`*`

<table id="simpletable_9AF29AA336C4447BBC2FD4A7D43ED91B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> string</span> </p> </td> 
  <td class="stentry"> <p>Message string. </p></td> 
 </tr> 
</table>

The HTTP response is not cacheable. An empty response is returned with MIME type `text/plain`. 
