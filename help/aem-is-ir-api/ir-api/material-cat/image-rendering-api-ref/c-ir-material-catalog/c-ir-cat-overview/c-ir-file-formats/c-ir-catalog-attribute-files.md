---
title: Catalog attribute files
description: Catalog attribute files can have any name, but must have an .ini file suffix. They can be readily maintained using any text editor.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b5afb99-3201-4e43-93e7-e8998354204f
---
# Catalog attribute files{#catalog-attribute-files}

Catalog attribute files can have any name, but must have an `.ini` file suffix. They can be readily maintained using any text editor.

Catalog attribute files consist of a set of text records, separated by a single `<CR>` (ASCII code 0xD), a single `<LF>` (ASCII code 0xA), or a `<CR><LF>` pair. Each record consists of an attribute name and one or more comma-separated attribute values:

`*`name`*= *`value`*&#42;[, *`value`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name </span> </span> </p> </td> 
  <td class="stentry"> <p>Attribute name; may consist of one or more letters, number, - (hyphen), and _ (underscore); not case-sensitive.</p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
  <td class="stentry"> <p>Attribute value; must not include <span class="codeph"> &lt;CR&gt; </span>, or <span class="codeph"> &lt;LF&gt; </span> characters, unless escaped by a single backslash just before the newline character. </p> </td> 
 </tr> 
</table>

* White space between tokens is optional. 
* The [!DNL Platform Server] ignores records with unknown attribute names. 
* Attribute names can consist of any combination of ASCII letters, numbers, and `-`, `_`, and `.` characters. 
* If the same attribute name occurs more than once in the same attribute file, the last one encountered prevails. 
* Use `#` as the first character to mark any record as a comment that the parser ignores.
