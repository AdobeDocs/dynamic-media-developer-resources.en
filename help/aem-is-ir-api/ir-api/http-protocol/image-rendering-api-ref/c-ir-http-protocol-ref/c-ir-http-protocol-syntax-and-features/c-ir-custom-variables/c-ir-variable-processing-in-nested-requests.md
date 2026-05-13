---
title: Variable processing in nested requests
description: $var$ references may occur anywhere within the curly braces of a nested Image Serving or Image Rendering request, including to the left of the '?' separating the path from the query.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa82ec48-aeec-4cd9-8d2e-cf9c913c67a7
TQID: 'https://experienceleague.adobe.com/m7BlSGU8gSozgp8fvNcWuMz5uvpUrfMi4fV5yCYH5bs'
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
# Variable processing in nested requests{#variable-processing-in-nested-requests}

$var$ references may occur anywhere within the curly braces of a nested Image Serving or Image Rendering request, including to the left of the '?' separating the path from the query.

The server substitutes these references with values (either from the url or from `catalog::Modifier` of the main image catalog) before further parsing and processing of the nested request.

In addition, all `$ *[!DNL var]*=` definitions from the url and `catalog::Modifier` are forwarded to all nested Image Serving and Image Rendering requests. Doing so ensures that all variable definitions are available to all templates, regardless of nesting level.

Regardless of the nesting level, only single-pass HTTP-encoding must be applied to variable values which are to be substituted anywhere in nested Image Rendering or Image Serving requests.
