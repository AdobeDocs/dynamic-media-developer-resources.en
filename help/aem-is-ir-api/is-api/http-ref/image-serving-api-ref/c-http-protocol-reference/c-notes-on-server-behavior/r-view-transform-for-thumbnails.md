---
description: The image returned to the client in response to a req=tmb request is derived from the composite image by considering the following values  wid=, hei=, attribute DefaultThumbPix, and attribute MaxPix.
solution: Experience Manager
title: View transform for thumbnails
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
TQID: https://experienceleague.adobe.com/d7WBX4YTHhcW8IOpn-PBeVj-7uFobTGnF2B-nFm5pug
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
# View transform for thumbnails{#view-transform-for-thumbnails}

The image returned to the client in response to a req=tmb request is derived from the composite image by considering the following values: wid=, hei=, attribute::DefaultThumbPix, and attribute::MaxPix.

1. **Calculate the view rect** - Use `wid=` or the width value of `attribute::DefaultThumbPix` for the width of the view rect. Use `hei=` or the height value of `attribute::DefaultThumbPix` for the height. The view rect must be fully specified in this step. (Note that the view rect is the same as the layer 0 rect, if no `size=`is specified for layer 0). 
1. **Scale the composite** - If `catalog::ThumbType=Crop`, then the composite is scaled to the smallest image possible while still filling the entire view rect; extra image data is cropped off. If `catalog::ThumbType= Fit`, then the composite is scaled to the largest image possible while still fitting the entire composite into the view rect. If `catalog::ThumbType=Texture`, the composite is not scaled at all to preserve the resolution specified in `catalog::ThumbRes`. 
1. **Fill and crop** - The view rect is filled with the `bgc=` color (or, if not specified, with `attribute::ThumbBkgColor`). The scaled composite is aligned with the view rect using attribute:: `ThumbHorizAlign` and attribute:: `ThumbVertAlign`. The scaled composite is then merged with the filled view rect without further scaling. Any areas of the composite that extend beyond the view rect are cropped off.
