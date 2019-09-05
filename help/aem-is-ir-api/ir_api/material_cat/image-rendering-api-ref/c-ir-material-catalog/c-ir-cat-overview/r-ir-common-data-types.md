---
description: Catalog attributes and fields may contain data of one of the following types.
seo-description: Catalog attributes and fields may contain data of one of the following types.
seo-title: Common data types
solution: Experience Manager
title: Common data types
topic: Scene7 Image Serving - Image Rendering API
uuid: a3e85730-31ee-40d7-a928-a6c4fdfbf45e
index: y
internal: n
snippet: y
---

# Common data types{#common-data-types}

Catalog attributes and fields may contain data of one of the following types.

 **Color**

Color value. Hexadecimal, packed RGB value, optionally preceded by 0x. For example, the RGB value `128,255,0` can be specified as `0x80ff00` or `80ff00`.

**Flag**

`0`=false, `1`=true, any other value means unknown or unspecified.

**Enum**

0 indicates an unknown or unspecified value, same as an empty field. Valid `enum` values are consecutive integer numbers, starting with 1.

**Integer number**

Signed integer value (e.g. 0, -12, 34). 0 or negative values may have special meaning.

**Real number**

Signed floating point value (e.g. `0, 12.5, 245 , -2.34e4`). 0 or negative values may have special meaning.

**Text string**

String delimiters are optional, unless the string contains any `<CR>`, `<LF>`, or `<TAB>` characters. Either single and double quotation marks may be used as delimiters. If quotation marks are used, any such quotation mark embedded within the string must be escaped by using two consecutive quotation marks (e.g. ' `This month''s Special`'). 
