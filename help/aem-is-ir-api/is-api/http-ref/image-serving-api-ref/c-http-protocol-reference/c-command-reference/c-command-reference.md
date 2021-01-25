---
description: This section describes the HTTP protocol commands.
seo-description: This section describes the HTTP protocol commands.
seo-title: Command reference
solution: Experience Manager
title: Command reference
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 72c4ed61-3436-4df5-b586-77808fb1903a
---

# Command reference{#command-reference}

This section describes the HTTP protocol commands.

**For Dynamic Media in AEM only**: Beyond the basic image settings that are available in the user interface, [!DNL Dynamic Media] in AEM ( [!DNL Adobe Experience Manager]) supports numerous advanced image modifications that you can specify in the **Image Modifiers** field. These parameters are defined below. Be aware, however, that the following functionality is not supported in Dynamic Media in AEM.

* Color correction commands: `icc=` and `iccEmbed=`. 
* Basic templating and text rendering commands: `text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=` and `textPs=`. 
* Localization commands: `locale=` and `req=xlate`. 
* `req=set` is not available for general usage. 
* `req=mbrset` 
* `req=saveToFile` 
* `req=targets` 
* `template=` 
* Non-core Dynamic Media services: SVG, Image Rendering, and Web-to-Print.

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

See also the Dynamic Media [Image Preset Options](https://docs.adobe.com/content/help/en/experience-manager-65/assets/dynamic/managing-image-presets.html#image-preset-options) in the AEM 6.5 documentation. 

* [align](r-align.md)
* [anchor](r-anchor.md)
* [bfc](r-bfc.md)
* [bgc](r-bgc.md)
* [bgColor](r-bgcolor.md)
* [blendMode](r-blendmode.md)
* [cache](r-is-http-cache.md)
* [clipPath](r-clippath.md)
* [clipXPath](r-clipxpath.md)
* [color](r-color-commandref.md)
* [crop](r-crop.md)
* [cropPathE](r-croppath.md)
* [defaultImage](r-is-http-defaultimage.md)
* [effect](r-effect.md)
* [effectMask](r-effectmask.md)
* [extend](r-extend.md)
* [fit](r-fit.md)
* [flip](r-flip.md)
* [fmt](r-is-http-fmt.md)
* [hei](r-is-http-hei.md)
* [hide](r-hide.md)
* [icc](r-icc.md)
* [iccEmbed](r-iccembed.md)
* [id](r-id.md)
* [imageSet](r-imageset.md)
* [jpegSize](r-jpegsize.md)
* [layer](r-layer.md)
* [locale](r-locale.md)
* [map](r-map.md)
* [mask](r-mask.md)
* [maskUse](r-maskuse.md)
* [op_blur](r-op-blur.md)
* [op_brightness](r-op-brightness.md)
* [op_colorbalance](r-op-colorbalance.md)
* [op_colorize](r-op-colorize.md)
* [op_contrast](r-op-contrast.md)
* [op_grow](r-op-grow.md)
* [op_growMask](r-op-growmask.md)
* [op_growMaskR](r-op-growmaskr.md)
* [op_hue](r-op-hue.md)
* [op_invert](r-op-invert.md)
* [op_noise](r-op-noise.md)
* [op_saturation](r-op-saturation.md)
* [op_sharpen](r-op-sharpen.md)
* [op_usm](r-op-usm.md)
* [op_usmR](r-op-usmr.md)
* [opac](r-opac.md)
* [origin](r-origin.md)
* [pathAttr](r-pathattr.md)
* [pathEmbed](r-pathembed.md)
* [perspective](r-perspective.md)
* [pos](r-pos.md)
* [printRes](r-printres.md)
* [pscan](r-pscan.md)
* [qlt](r-is-http-qlt.md)
* [quantize](r-is-http-quantize.md)
* [rect](r-rect.md)
* [req](r-req/r-req.md)
* [res](r-res.md)
* [resMode](r-is-http-resmode.md)
* [rgn](r-rgn.md)
* [rotate](r-rotate.md)
* [scale](r-is-http-scale.md)
* [scl](r-scl.md)
* [size](r-size-reference.md)
* [src](r-src.md)
* [template](r-template.md)
* [text](r-text.md)
* [textAngle](r-textangle.md)
* [textAttr](r-textattr.md)
* [textFlowPath](r-textflowpath.md)
* [textFlowXPath](r-textflowxpath.md)
* [textPath](r-textpath.md)
* [textPs](r-textps.md)
* [type](r-type.md)
* [wid](r-is-http-wid.md)
* [xmpEmbed](r-xmpembed.md)
