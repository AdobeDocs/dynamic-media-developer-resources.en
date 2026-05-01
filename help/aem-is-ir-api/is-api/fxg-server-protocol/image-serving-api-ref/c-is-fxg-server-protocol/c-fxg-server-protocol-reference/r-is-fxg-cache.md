---
description: Cache control. Allows selectively disabling client-side caching (browser, proxy servers, network caching systems) and caching in the internal [!DNL Platform Server] cache.
solution: Experience Manager
title: cache
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 622c36fa-c209-4149-a7db-85067215b5e5
TQID: https://experienceleague.adobe.com/oYnkiGCpgbDfh9QpTPmJtyrH6F2CLxNBILCK3lChwcw
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
# cache{#cache}

Cache control. Allows selectively disabling client-side caching (browser, proxy servers, network caching systems) and caching in the internal [!DNL Platform Server] cache.

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
