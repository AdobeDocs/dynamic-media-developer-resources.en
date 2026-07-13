---
title: Vignette Converter
description: The Vignette Converter (vntc) is a command-line utility used to prepare content created with Image Authoring for deployment with Image Rendering.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9e2ad2d4-9061-41d1-941b-8be4c17a6c43
TQID: 'https://experienceleague.adobe.com/NZsbUGCd25rHyvrmt-Rh3XN0p3pHqEtGZrXLp-7JBsc'
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
# Vignette Converter{#vignette-converter}

The Vignette Converter (vntc) is a command-line utility used to prepare content created with Image Authoring for deployment with Image Rendering.

 [!DNL vntc] is in [!DNL *[!DNL install_root]*\ImageServing\bin]. It has the following capabilities:

* Converts primary vignettes to single-resolution, multi-resolution, or pyramid production vignettes (see [Vignette Scaling](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)). 
* Produces production cabinet and window covering style files (see `-resolution` and `-jpegquality`). 

* Produce different file versions of vignettes, cabinets, and window coverings style files for use with older versions of Image Rendering. 
* Extracts view images from vignettes, either full resolution or thumbnails (see `-thumbwidth` and `-image`). 
* Extracts relevant properties from the source file (see `-info`) and sends them to `stdout` or an optional log file (see `-log`).

While the use of [!DNL vntc] is optional, Adobe recommends its use for the best server performance. The Vignette Converter also implements extensive error checking and can prevent serious server issues, including crashes, when used diligently.

When generating production vignettes, the pixel width of the output vignette (or 0 if pyramid or multi-resolution vignettes) is appended to the name of the generated output vignette file. When processing cabinet style files, the output resolution is appended to the output file name. All output files, including the optional thumbnail, image, and log files and the production vignette or cabinet style file are placed in the same directory where *[!DNL sourceFile]* is located (unless `-destPath` is specified).

The Vignette Converter limits itself by default to at most 3 GB of memory. When vntc hits this limit, it stops processing and produces an error. This limit can be changed using `-maxmem`.

>[!NOTE]
>
>The Vignette Update Tool in Image Authoring can also be used to prepare vignettes for Image Rendering use. Similarly, the Content Authoring Tool can generate cabinet style files for use with Image Rendering. Use [!DNL vntc] if processing is to be automated. The tools in Image Authoring include a graphical user interface, thus are typically easier to use interactively.

## See also {#section-3c756bf17b634543904fdd928adeafb2}

Image Authoring Documentation

