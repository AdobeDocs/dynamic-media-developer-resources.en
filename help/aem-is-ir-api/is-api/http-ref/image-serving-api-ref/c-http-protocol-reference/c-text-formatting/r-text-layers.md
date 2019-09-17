---
description: textPs= supports a number of different usage models described in this section.
seo-description: textPs= supports a number of different usage models described in this section.
seo-title: Text layers
solution: Experience Manager
title: Text layers
topic: Scene7 Image Serving - Image Rendering API
uuid: 9ccef969-7c54-49ce-b6ff-ae4eabfcf99b
---

# Text layers{#text-layers}

textPs= supports a number of different usage models described in this section.

>[!NOTE] {class="- topic/note "}
>
>This section does not apply to `text=`.

Common rules and definitions are as follows:

* Self-sizing text layers are layers which do not include a `size=` command or for which `size=0,0` is specified. 

* The layer size of self-sizing text layers is determined by the actual text rendered. 
* The default layer anchor of self-sizing text layers generally is *not* at the center of the layer (see below). 
* If `anchor=` or `origin=` is specified for self-sizing text layers, the position of the text layer is influenced by the text content. 

* When `size=` is specified, parts of character glyphs may be rendered outside the layer rectangle. 
* `pos=` can be used in all cases to reposition a text layer.

## Point text (self-sizing) {#section-db99ec98eb114458b2dbc9911a58f74a}

Photoshop-style point text is simulated when `textPs=` is specified without `size=`, `textPath=`, or `textFlowPath=`. The layer size is determined horizontally by the width of the rendered text and vertically by the line spacing. Text will never wrap automatically.

If neither `anchor=` nor `origin=` are specified, the first line of the text is positioned immediately above the layer origin; paragraphs marked with `\ql` are positioned to the right of the layer origin, paragraphs which include `\qr` are rendered to the left of the origin, and paragraphs with `\qc` are centered horizontally around the origin. Standard layer positioning rules apply if `anchor=` or `origin=` are specified.

If `color=` is specified, it fills the bounding box of the actual text rendered.

The following RTF commands are ignored: `\qj`, `\marg*`, `\hyph*`, `\vertal*`.

## Rectangular text box {#section-1d3ab11df26d4004a1a801546756475d}

If `size=` is specified in addition to `textPs=` (without `textPath=` and `textFlowPath=`), text is constrained to the specified rectangle. The layer is positioned as usual. Character glyphs near the text box edges may be rendered partially outside the text box.

`color=` fills the region defined by `size=`.

All RTF commands are applied as expected.

## Variable height text box {#section-e1233d1c9f8e43218667361dc0c4fd06}

Specifying `size=` with 0 height allows the text box to be sized vertically to accommodate all contents. The layer width is defined by the width of `size=`, and the layer height by the height of the actual rendered text. The layer is positioned as usual. Character glyphs near the left and right edges of the text box may be rendered partially outside the text box.

`color=` fills the rectangle defined by the width specified with `size=` and the height of the actual text rendered.

The following RTF commands are ignored:

`\vertal*`

## Self-sizing text in path {#section-d26685e7085847efaaeba64b9cb5ed9f}

`textFlowPath=` in conjunction with `textPs=` can be used to define one or more regions into which text should be flowed. `textFlowXPath=` may be specified optionally to exclude text from flowing into one or more areas. If `size=` is not specified, the resulting text layer is self-sizing and the layer size is determined by the bounding box of the text actually rendered.

If neither `origin=` nor `anchor=` are specified, the layer anchor defaults to (0,0) of the pixel coordinate space used to define the path(s), ensuring absolute positioning regardless of the rendered text. If `anchor=` or `origin=` are specified, the layer is positioned relative to (and adapting to) the bounding box of the actual contents rendered.

`color=` fills the bounding box of the actual text rendered.

The following RTF commands are ignored:

`\marg*`

## Pre-sized text in path {#section-ed492a8a54414cd4bde360500cec6968}

If `size=` is specified together with `textFlowPath=`, the layer size is pre-determined. (0,0) of the pixel coordinate space used to define the path(s) is located at the top-left corner of the layer rectangle.

The `textFlowPath=` regions may be located outside the layer rectangle. Text will always be flowed and rendered into all path regions, even if this results in text being rendered outside the layer rectangle. `extend=0,0,0,0`can be used to crop the rendered text to the layer rectangle.

For layer positioning purposes, the layer rectangle is based on the specified `size=`, regardless of how much text is actually rendered, even if some of it is located outside the layer rectangle. Standard layer positioning applies.

`color=` fills the rectangular area defined by `size=`.

The following RTF commands are ignored for `textFlowPath=`:

`\marg*`

## Self-sizing text on path {#section-7ce6b9b26b354ba381e4378703154062}

`textPath=` defines one or more paths onto which text specified with `textPs=` should be rendered. When `size=` is not specified, the resulting text layer is self-sizing. The layer size is determined by the bounding box of the actual text rendered.

If neither `origin=` nor `anchor=` are specified, the layer anchor defaults to (0,0) of the pixel coordinate space used to define the path; the position of the rendered text is fixed regardless of how much text is rendered. If `anchor=` or `origin=` are specified, the layer is positioned relative to (and adapting to) the bounding box of the actual contents rendered.

`color=` fills the bounding box of the actual text rendered.

The following RTF commands are ignored:

* `\marg*` 
* `\hyph*` 
* `\vertal*`

Any text after the first `\par` or `\line` is ignored.

## Pre-sized text on path {#section-a3bbbc5187f448b192e53d27e2c53f2f}

If `size=` is specified together with `textPath=`, the layer size is pre-determined. (0,0) of the pixel coordinate space used to define the path(s) is located at the top-left corner of the layer rectangle.

The paths may be located partially or entirely outside the layer rectangle. Text will always be applied and rendered along the entire path, even if outside the layer rectangle. `extend=0,0,0,0` can be used to crop the rendered text to the layer rectangle.

For layer positioning purposes, the layer rectangle is based on the specified `size=`, even if some of the text is rendered outside the layer rectangle. Standard layer positioning applies.

`color=` fills the area defined by `size=`.

The following RTF commands are ignored:

* `\marg*` 
* `\q*` 
* `\marg*` 
* `\hyph*` 
* `\vertal*`

Any text after the first `\par` or `\line` is ignored. 
