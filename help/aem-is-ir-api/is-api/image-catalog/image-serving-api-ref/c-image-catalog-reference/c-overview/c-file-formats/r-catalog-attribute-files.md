---
description: Catalog attribute files can have any name, but must have an .ini file suffix. They can be readily maintained using any text editor.
solution: Experience Manager
title: Catalog attribute files
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79d9439d-7749-4ae1-aa73-e88e01cf7555
TQID: 'https://experienceleague.adobe.com/RCxeXg3wb10jo37biAs1puqmEo8bAL-i-oZBwGHuloA'
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
# Catalog attribute files{#catalog-attribute-files}

Catalog attribute files can have any name, but must have an .ini file suffix. They can be readily maintained using any text editor.

Catalog attribute files consist of a set of text records, separated by a single `<CR>` (ASCII code `0xD`), a single `<LF>` (ASCII code `0xA`), or a `<CR><LF>` pair. Each record consists of an attribute name and one or more comma-separated attribute values:

`*`name`*= *`values`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> values</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[,<span class="varname"> values</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p> </td> 
  <td class="stentry"> <p>Attribute name. May consist of one or more letters, number, -, and _. Not case-sensitive. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Attribute value. Must not include <span class="codeph"> &lt;CR&gt;</span> or <span class="codeph"> &lt;LF&gt;</span> characters, unless escaped by a single backslash just before the newline character. </p></td> 
 </tr> 
</table>

White space between tokens is optional.

Records with unknown attribute names are ignored by the [!DNL Platform Server].

Attribute names may consist of any combination of ASCII letters, numbers, as well as "-", "_", and ".".

If the same attribute name occurs more than once in the same attribute file, the last one encountered prevails.

Use # as the first character to mark any record as a comment, which the parser ignores.
