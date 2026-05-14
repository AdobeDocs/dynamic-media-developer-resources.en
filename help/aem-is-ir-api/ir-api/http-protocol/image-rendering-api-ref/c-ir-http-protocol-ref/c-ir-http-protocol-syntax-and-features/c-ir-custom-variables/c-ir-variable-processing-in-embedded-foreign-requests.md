---
title: Variable processing in embedded foreign requests
description: $var$ references occurring anywhere within the curly braces of an embedded foreign request are substituted with matching variable definition values.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
TQID: 'https://experienceleague.adobe.com/-0KT9d6qz9-8d41vKNgbCYUKQQLBRaLE-0TFmyIvRCM'
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
# Variable processing in embedded foreign requests{#variable-processing-in-embedded-foreign-requests}

Any `$var$` references that occur anywhere within the curly braces of an embedded foreign request are substituted with matching variable definition values.

Allows embedded foreign requests to be placed in a template in an image catalog.

Variable values which are to be substituted into foreign requests typically must be double-encoded, because no re-encoding is applied before the server attempts to transmit the final foreign url.
