---
description: Image Serving supports image catalogs with ISO‑8859‑1 and UTF‑8 encoding.
solution: Experience Manager
title: Character encoding
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: e6e50c2a-53d3-4776-a3f6-4a9d3407e562
---
# Character encoding{#character-encoding}

Image Serving supports image catalogs with ISO‑8859‑1 and UTF‑8 encoding.

A byte order mark (BOM) is used to specify the encoding for each file. For UTF-8, the BOM is the byte sequence `EF BB BF`. UTF-8 encoding is assumed when this character sequence is detected at the very beginning of each image catalog file. Any other byte sequence results in the file being interpreted as being encoded to the ISO-8859-1 standard.

Many contemporary applications, when configured for UTF-8, inserts the BOM automatically.
