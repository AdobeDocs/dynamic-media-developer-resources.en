---
description: Image Serving provides several alternatives to render text, accessible with the text= and textPs= commands.
seo-description: Image Serving provides several alternatives to render text, accessible with the text= and textPs= commands.
seo-title: Text formatting
solution: Experience Manager
title: Text formatting
topic: Scene7 Image Serving - Image Rendering API
uuid: e67b6dd2-2a78-4014-9525-816d91c9e783
---

# Text formatting{#text-formatting}

Image Serving provides several alternatives to render text, accessible with the text= and textPs= commands.

 `textPs=` provides a high level of similarity with text rendered with Adobe Photoshop and Illustrator. `text=` is reasonably compatible with text rendered with Windows Wordpad.

>[!NOTE]
>
>In addition to the differences listed elsewhere, `text=` produces subtle differences in the rendered text when compared with `textPs=`. For example, underlines do not have the same thickness and position and synthesized italics are rendered at a slightly different angle. If text does not fit into the available space, `text=` may partially crop the last line, while `textPs=` will only render complete lines.

All text commands accept formatted text based on a subset of the RTF (Rich Text Format) specification. Each text layer may specify a different text command.

The following table lists the key features available for each text command: 

<table id="table_9C41CBDA94C24805B538E5049B0137C6"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Feature</b> </th> 
   <th class="entry"> <b> text=</b> </th> 
   <th class="entry"> <b> textPs=</b> </th> 
   <th class="entry"> <b> See also</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> Adobe Photoshop-compatible </p> </td> 
   <td> <p> no </p> </td> 
   <td> <p> limited </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Flow text into arbitrary shapes </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>textFlowPath=, textFlowXPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Flow text along arbitrary paths </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>textPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Copy-fitting </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>yes </p> </td> 
   <td> Copy-Fitting <p>, \copyfit, \copyfitlines, \copyfitmaxlines </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Text box margins </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>\margl, \margr, \margt, \margb </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Full paragraph justification </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>\qj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>last line justification </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>\lastql, \lastqr, \lastqc, \lastqj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Paragraph indentation </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>\fi, \li, \ri </p> </td> 
  </tr> 
  <tr> 
   <td> <p>All caps and small caps text </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>\caps, \scaps </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Image Serving colors </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>\*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Multiple anti-aliasing modes </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>top-bottom/right-left text flow </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>\stextFlow </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Photofont® support </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>yes </p> </td> 
   <td> Font Handling </td> 
  </tr> 
  <tr> 
   <td> <p>Auto-size layer to fit text </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>text=, textId=, size= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>CMYK support </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>\cmykcolortbl, \*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Right-to-left character flow </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>\rtlch </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Disable word-wrap </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Auto-scale text to fit layer (by varying resolution) </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

RTF-compliant strings can be assembled manually or by formatting the desired text in a text editor or word processor capable of saving RTF files. The RTF file may then be opened in a plain text editor, and the relevant raw RTF content of the file copied to the request URL.

Some word processors generate rather large files, which include substantial preambles that are not used by Scene7 Image Serving. It is recommended to remove the unused RTF elements from the string before passing the string to the text commands.

Language-encoding based on UTF-8 and ISO standards is supported in RTF strings as an alternative to the standard RTF character encoding mechanisms. This allows applications to send non-English text to the server without knowledge of RTF encoding.

All non-HTTP compliant characters must be properly escaped, if the string is to be transmitted via http. Only '=', '&', and '%' need to be escaped if the string is incorporated into the `catalog::Modifiers` field of an image catalog record. Control characters, including `<CR>`, `<LF>`, and `<TAB>` should always be removed.

The Image Serving text engines interpret a sub-set of commands defined by the Rich Text Format (RTF) Specification, version 1.6. This sub-set is focused on font/character formatting, simple paragraph formatting, and support for international fonts and character sets. More advanced formatting constructs, such as style sheets and tables, are not supported at this time.

Familiarity with the Rich Text Format (RTF) Specification, as published by Microsoft, is required when attempting to construct RTF-encoded text strings manually. 

* [Font handling](r-font-handling.md)
* [Color handling](r-color-handling.md)
* [Copy-fitting](r-copy-fitting.md)
* [Text layers](r-text-layers.md)
* [Text positioning](r-text-positioning.md)
* [Reserved characters](r-reserved-characters.md)
* [Supported RTF commands and keywords](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [RTF encoding examples](r-rtf-encoding-examples.md)
