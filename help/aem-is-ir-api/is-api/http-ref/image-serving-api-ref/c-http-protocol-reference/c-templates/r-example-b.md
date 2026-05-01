---
description: Similar requirements as Example A, but use a solid color background and allow the height of the composite to vary, to accommodate images with different aspect ratios.
solution: Experience Manager
title: Example B
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90ef96fc-c12f-4fc8-b465-6520b71f4e7b
TQID: https://experienceleague.adobe.com/mfQRtZ3Uh4-L6XiGLUAe5LjXnWC4R1-96xgf9SGRFHQ
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
# Example B{#example-b}

Similar requirements as Example A, but use a solid color background and allow the height of the composite to vary, to accommodate images with different aspect ratios.

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> catalog::Id</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> catalog::Modifier</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+goes+here&amp; layer=0&amp;size=800,0&amp;extend=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp; layer=1&amp;text=rtf…$text$…rtf-encoding&amp;rotate=-90&amp;originN=.5,0&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

The image is placed in layer 0, and the height value of `size=` is set to 0. This setting causes the actual height to be determined by the height of the image after scaling it to 800 pixels wide.

The variable `extend=` adds 100 pixels to the top and bottom, and 200 pixels to the right.

The origins for both layer 0 and layer 1 are placed at the center-right of the compositing area, to achieve the desired text position.

The following image shows the composite result for different aspect ratios of the image and different text strings.

![Example B image](assets/exampleb.png)
