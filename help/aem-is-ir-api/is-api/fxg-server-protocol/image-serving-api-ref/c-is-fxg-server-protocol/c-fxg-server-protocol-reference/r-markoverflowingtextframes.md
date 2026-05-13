---
description: Display overset text frames with plus sign. A text overflow indicator shows when text exceeds the space allocated for it in a text frame (or in the last text frame in the case of threaded text). The indicator is a red box with a plus sign in it.
solution: Experience Manager
title: markOverflowingTextFrames
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1e2a3d4-ef1f-4d5e-be9c-eeec36f46603
TQID: 'https://experienceleague.adobe.com/Wy5VLpT5I1KzXUrKaPoetj2ejv4wbUOsU1My9vEA5gM'
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
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# markOverflowingTextFrames{#markoverflowingtextframes}

Display overset text frames with plus sign. A text overflow indicator shows when text exceeds the space allocated for it in a text frame (or in the last text frame in the case of threaded text). The indicator is a red box with a plus sign in it.

<table id="simpletable_F17FD29EB52043BF9000923ED5195A26"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;markOverflowingTextFrames</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

Setting modifier `markOverflowingTextFrames=1` through a URL call marks all the text frames where text is overset with a plus sign. Also, in Dynamic Media Classic previewer, the text overset indicator is set to " `TRUE`" by default.

Default is 0.
