---
title: Usage
description: This topic describes vntc usage syntax.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b892fe86-1b7c-4a49-a1cd-473f51d04d10
TQID: 'https://experienceleague.adobe.com/uNh-n1OEJ5gxWBjLbBNutrNJ1Osae-PEOFBmaKNVf6c'
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
# Usage{#usage}

This topic describes vntc usage syntax.

 `vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* is the path and name of the file to be processed. It can be a path relative to the current working directory or an absolute path. It must be a valid vignette, cabinet style, or window covering style file and have one of the following suffixes: 

* [!DNL .vnt]
* [!DNL .vnc]
* [!DNL .vnw]

Required.

*[!DNL destFile]* is the path and name for the output vignette file. If not specified, the output file is placed in the folder specified with `-destpath`. In this scenario, the file name is automatically generated from the input file name and a size suffix, separated with the string specified with `-separator`. For vignettes, the size suffix is the pixel width of the single-resolution output vignette, the width of the first view of a multi-resolution output vignette, or '0' if there is a pyramid vignette. For cabinet style files, the output resolution is used as the file suffix. *[!DNL destFile]* is ignored when `-info` is specified.

