---
description: Image Rendering supports material catalogs with ISO‑8859‑1 and UTF‑8 encoding.
solution: Experience Manager
title: Character encoding
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: ee7b33fd-7607-4bff-867b-6e7a837a9ed4
---
# Character encoding{#character-encoding}

Image Rendering supports material catalogs with ISO‑8859‑1 and UTF‑8 encoding.

A byte order mark (BOM) is used to specify the encoding for each file. For UTF-8, the BOM is the byte sequence `EF BB BF`. UTF-8 encoding is assumed when this character sequence is detected at the very beginning of each material catalog file. Any other byte sequence result in the file being interpreted as being encoded to the ISO-8859-1 standard.

Many contemporary applications, when configured for UTF-8, insert the BOM automatically.
