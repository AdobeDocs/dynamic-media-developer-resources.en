---
title: Character encoding
description: Image Rendering supports material catalogs with ISO‑8859‑1 and UTF‑8 encoding.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ee7b33fd-7607-4bff-867b-6e7a837a9ed4
TQID: 'https://experienceleague.adobe.com/1ITLimvCUD8hrdfeyyod6nE0sMmfIJ3ySx5HCFa2ZQk'
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
# Character encoding{#character-encoding}

Image Rendering supports material catalogs with ISO‑8859‑1 and UTF‑8 encoding.

A byte order mark (BOM) is used to specify the encoding for each file. For UTF-8, the BOM is the byte sequence `EF BB BF`. UTF-8 encoding is assumed when this character sequence is detected at the very beginning of each material catalog file. Any other byte sequence result in the file being interpreted as being encoded to the ISO-8859-1 standard.

Many contemporary applications, when configured for UTF-8, insert the BOM automatically.

