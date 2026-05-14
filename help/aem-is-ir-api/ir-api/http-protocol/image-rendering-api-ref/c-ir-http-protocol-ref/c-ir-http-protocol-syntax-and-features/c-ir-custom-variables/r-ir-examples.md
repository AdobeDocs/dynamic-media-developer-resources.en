---
title: Examples
description: This example uses Image Serving to colorize an object and apply a decal containing custom text in one of a set of vignettes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 85f11642-e1ff-4bf0-bd21-d419805cff4a
TQID: 'https://experienceleague.adobe.com/GMzKDuP-wzTrPJQbxpXc0M08BjCQdWCkGo5jOUiWipU'
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
# Examples{#examples}

This example uses Image Serving to colorize an object and apply a decal containing custom text in one of a set of vignettes.

IR variables are used to identify the vignette, the logo image, and the custom text.

The `vignette::Modifier` field in the record named *template* in the vignette map of the material catalog `myCat` contains the following:

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

All used vignettes are listed in the vignette map of the material catalog `myCat`.

The client can now make the following request to retrieve the default image (uses the variables defined at the beginning of the template):

[!DNL `https://server/myCat/template`]

The following request specifies certain content to render:

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

Refer to Image Serving Documentation for details about the Image Serving `text=` command.
