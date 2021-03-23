---
description: The Vignette Converter (vntc) is a command line utility used to prepare content created with Image Authoring for deployment with Image Rendering.


solution: Experience Manager
title: Vignette Converter

feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# Vignette Converter{#vignette-converter}

The Vignette Converter (vntc) is a command line utility used to prepare content created with Image Authoring for deployment with Image Rendering.

 [!DNL vntc] is located in [!DNL *[!DNL install_root]*\ImageServing\bin]. It has the following capabilities:

* Converts primary vignettes to single resolution, multi-resolution, or pyramid production vignettes (see [Vignette Scaling](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)). 
* Produces production cabinet and window covering style files (see `-resolution` and `-jpegquality`). 

* Can produce different file versions of vignettes, cabinets, and window coverings style files for use with older versions of Image Rendering. 
* Extracts view images from vignettes, either full resolution or thumbnails (see `-thumbwidth` and `-image`). 
* Extracts relevant properties from the source file (see `-info`) and sends them to `stdout` or an optional log file (see `-log`).

While the use of [!DNL vntc] is optional, it is highly recommended for best server performance. [!DNL vntc] also implements extensive error checking and can prevent serious server issues, including crashes, when used diligently.

When generating production vignettes, the pixel width of the output vignette (or 0 in case of pyramid or multi-resolution vignettes) is appended to the name of the generated output vignette file. When processing cabinet style files, the output resolution is appended to the output file name. All output files, including the optional thumbnail, image, and log files as well as the production vignette or cabinet style file are placed in the same directory where *[!DNL sourceFile]* is located (unless `-destPath` is specified).

[!DNL vntc] limits itself by default to at most 3GB of memory. When Vntc hits this limit it will stop processing and will produce an error. This limit can be changed using `-maxmem`.

>[!NOTE]
>
>The Vignette Update Tool in Image Authoring can also be used to prepare vignettes for Image Rendering use. Similarly, the Content Authoring Tool is capable of generating cabinet style files for use with Image Rendering. Use [!DNL vntc] if processing is to be automated. The tools in Image Authoring include a graphical user interface, thus are typically easier to use interactively.

## See also {#section-3c756bf17b634543904fdd928adeafb2}

Image Authoring Documentation 
