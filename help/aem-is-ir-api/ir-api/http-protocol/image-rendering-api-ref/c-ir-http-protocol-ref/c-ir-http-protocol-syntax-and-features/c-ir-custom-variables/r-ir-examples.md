---
description: This example uses Image Serving to colorize an object and apply a decal containing custom text in one of a set of vignettes.
solution: Experience Manager
title: Examples
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# Examples{#examples}

This example uses Image Serving to colorize an object and apply a decal containing custom text in one of a set of vignettes.

IR variables are used to identify the vignette, the logo image, and the custom text.

The `vignette::Modifier` field in the record named *template* in the vignette map of the material catalog `myCat` contains the following:

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

All vignettes that will be used are listed in the vignette map of the material catalog `myCat`.

The client can now make the following request to retrieve the default image (this uses the variables defined at the beginning of the template):

[!DNL `https://server/myCat/template`]

The following request specifies certain content to render:

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

Refer to Image Serving Documentation for details about the Image Serving `text=` command. 
