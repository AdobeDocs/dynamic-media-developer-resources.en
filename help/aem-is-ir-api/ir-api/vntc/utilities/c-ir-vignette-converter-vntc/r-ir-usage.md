---
description: This topic describes vntc usage syntax.
seo-description: This topic describes vntc usage syntax.
seo-title: Usage
solution: Experience Manager
title: Usage
uuid: 251aa1a0-5f19-42ab-b237-3e3b53fe8320
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Business Practitioner"
---

# Usage{#usage}

This topic describes vntc usage syntax.

 `vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* is the path and name of the file to be processed. Can be a path relative to the current working directory or an absolute path. Must be a valid vignette, cabinet style, or window covering style file and have one of these suffixes: [!DNL .vnt], [!DNL .vnc], or [!DNL .vnw]. Required.

*[!DNL destFile]* is the path and name for the output vignette file. If not specified, the output file is placed in the folder specified with `-destpath`. In this scenario, the file name is automatically generated from the input file name and a size suffix, separated with the string specified with `-separator`. For vignettes, the size suffix is the pixel width of the single-resolution output vignette, the width of the first view of a multi-resolution output vignette, or '0' in case of a pyramid vignette. For cabinet style files, the output resolution is used as the file suffix. *[!DNL destFile]* is ignored when `-info` is specified. 
