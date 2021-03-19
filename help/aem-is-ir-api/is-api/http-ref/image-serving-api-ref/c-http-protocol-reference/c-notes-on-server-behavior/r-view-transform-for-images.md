---
description: View transform for images
solution: Experience Manager
title: View transform for images
uuid: 8594f746-0e58-4a59-933c-a44dc0b06c25
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Business Practitioner"
---

# View transform for images{#view-transform-for-images}

The image returned to the client in response to a `req=img` request is derived from the composite image by considering the following values: `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix`, and the size of the composite image.

If `wid=` and `hei=` are specified, and `scl=` is not, composite image is scaled so that it fits fully within the view rect defined by `wid=` and `hei=`. If the aspect ratio of the view rect is different than that of the composite image, then the scaled composite image is aligned within the view rect using the `align=` value, if specified, or it is centered otherwise. Any space not covered by image data is filled with `bgc=` or, if not specified, with `attribute::BkgColor`.

If `scl=` is specified, the composite image is scaled by that scale factor. If `wid=` and/or `hei=` is specified as well, the scaled image is then cropped to `wid=` and/or `hei=` or extra space is added, as needed. `align=` specifies where the image is cropped or extra space is added, and any extra space is filled with `bgc=` or `attribute::BkgColor`.

If neither `wid=`, `hei=` nor `scl=` are specified, and if either width or height of the composite image exceeds `attribute::DefaultPix`, then the composite image is scaled to not exceed `attribute::DefaultPix`. Otherwise, the composite image is used without scaling.

To guarantee that the view image is returned without any further scaling, specify `scl=1`.

If `rgn=` is specified, the reply image is then cropped accordingly to arrive at the final reply image size. This size is compared with `attribute::MaxPix` (if defined), and an error is generated if the reply image is larger in either dimension.

If `fmt=` specifies data without alpha, any transparent areas in the reply image are filled with `bgc=` or `attribute::BkgColor`. 
