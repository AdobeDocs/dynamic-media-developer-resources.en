---
description: Cache control. Allows selectively disabling client-side caching (browser, proxy servers, network caching systems) and caching in the internal Platform Server cache.
solution: Experience Manager
title: cache
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# cache{#cache}

Cache control. Allows selectively disabling client-side caching (browser, proxy servers, network caching systems) and caching in the internal Platform Server cache.

 `&cache= *`cacheControl`*`

`&cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_DA4D92F0AEF84FD49953876796058B7F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
</table>

If only one *`cacheControl`* value is specified, it is applied to both client and server caches.

Request attribute. Ignored when the request does not return a reply image. *`clientControl`* is ignored when client-side caching is disabled by the image catalog (if `catalog::Expiration` has a negative value).

Defaults to `cache=on,on`. 
