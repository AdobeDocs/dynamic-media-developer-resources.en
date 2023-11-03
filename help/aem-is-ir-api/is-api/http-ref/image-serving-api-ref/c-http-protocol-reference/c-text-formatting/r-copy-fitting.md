---
description: textPs= implements a proprietary copy-fitting algorithm which automatically adjusts the font sizes to optimally fill the text area with text, minimizing extra space at the bottom while avoiding overflow.
solution: Experience Manager
title: Copy-fitting
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1a560f3-f92c-4143-b80a-e1674c8a4207
---
# Copy-fitting{#copy-fitting}

textPs= implements a proprietary copy-fitting algorithm which automatically adjusts the font sizes to optimally fill the text area with text, minimizing extra space at the bottom while avoiding overflow.

Copy-fitting can be enabled and controlled collectively for the entire text layer, on a paragraph basis, even for an individual text span.

Specify the minimum font size with `\fs` and the maximum font size with `\copyfit`. Any number of ranges are permitted in the same RTF string. Sizes for all ranges are varied proportionally, ensuring that the desired font size ratios are maintained.

`\copyfit` is considered a character formatting command and has scope rules like `\fs` and `\b`.

Copy-fitting is disabled by specifying `\copyfit` with a size equal to or smaller than the size specified with `\fs`.

## Limiting the number of lines {#section-e5aee0f039e04842afc3d6884ed681ac}

In addition to specifying the range of font sizes, the behavior of the copy-fitting algorithm can be further controlled with the `\copyfitlines` or `\copyfitmaxlines` commands, which limit the number of lines the algorithm generates. Both commands accept a line count parameter or 0, to not limit the number of lines in the copy-fitted region.

`\copyfitlines` permits text to overflow to additional lines when it does not fit into the specified number of lines. Explicit line breaks in the text segment to be copy-fitted are always honored.

`\copyfitmaxlines` always truncates extra output lines which exceed the specified limit. The specified number of lines are never exceeded, even if explicit line breaks are present. For this release of Image Serving, no more than N-1 `\line` markers may be present in the copy-fitted text span. Behavior is undefined if this limit is exceeded.

## Examples {#section-f4ddbbfade444560be30a813d90c2c1b}

The following examples assume that bodies of text are provided with variables named *[!DNL $A$]*, *[!DNL $B$]*, and *[!DNL $C$]*.

**Maintain the same ratio between font sizes throughout the range:**

`{\fs10\copyfit100 $A${\fs20\copyfit200 $B$}$C$}`

*[!DNL $B$]* is always rendered twice as large as the rest of the text. When much text is specified, *[!DNL $A$]* and *[!DNL $C$]* is rendered with `\fs10` and *[!DNL $B$]* with `\fs20`. With little text, *[!DNL $A$]* and *[!DNL $C$]* use `\fs100` and *[!DNL $B$]* `\fs200`.

**Converge to a common large font size if only a small amount of text is drawn:**

`{\copyfit100\fs10 $A${\fs20 $B$}$C$}`

At the smallest end of the range, *[!DNL $B$]* is rendered with `\fs20`, twice as large as *[!DNL $A$]* and *[!DNL $C$]* at `\fs10`. All text is drawn at `\fs100` (50 pts) at the opposite end of the range.

**Converge to a common small font size if much text is to be rendered:**

`{\fs10\copyfit100 $A${\copyfit200 $B$}$C$}`

All text is drawn with \fs10 on the small end of the range, while at its largest, *[!DNL $A$]* and *[!DNL $C$]* are rendered with `\fs100` and *[!DNL $B$]* with `\fs200`.

**Disable copy-fitting for an inner text span:**

`{\fs10\copyfit100 $A${\fs50\copyfit0 $B$}$C$}`

The font size for *[!DNL $A$]* and *[!DNL $C$]* can vary between 10 and 100, while *[!DNL $B$]* is always rendered with `\fs50`.

**Limit the output to a single line, even if more vertical space is available, but permit it to overflow to additional lines if too much text is specified to fit into a single line at `\fs10`:**

`{\fs10\copyfit100 \copyfitlines1 $A$}`

**Limit the output to a single line, even if more vertical space is available. If too much text is specified to fit into a single line at `\fs10` it is truncated:**

`{\fs10\copyfit100 \copyfitmaxlines1 $A$}`
