---
title: Common data types
description: Catalog attributes and fields may contain data of one of the following types.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9af44474-0512-452a-af9e-48918e9da6ca
---
# Common data types{#common-data-types}

Catalog attributes and fields may contain data of one of the following types.

 **Color**

Color value. Hexadecimal, packed RGB value, optionally preceded by 0x. For example, the RGB value `128,255,0` can be specified as `0x80ff00` or `80ff00`.

**Flag**

`0`=false, `1`=true, any other value means unknown or unspecified.

**Enum**

`0` indicates an unknown or unspecified value, same as an empty field. Valid `enum` values are consecutive integer numbers, starting with 1.

**Integer number**

Signed integer value (for example `0, -12, 34`). `0` or negative values may have special meaning.

**Real number**

Signed floating point value (for example, `0, 12.5, 245 , -2.34e4`). 0 or negative values may have special meaning.

**Text string**

String delimiters are optional, unless the string contains any `<CR>`, `<LF>`, or `<TAB>` characters. Either single and double quotation marks may be used as delimiters. If quotation marks are used, any such quotation mark embedded within the string must be escaped by using two consecutive quotation marks (for example, ' `This month''s Special`').
