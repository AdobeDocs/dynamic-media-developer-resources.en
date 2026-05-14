---
title: Common data types
description: Catalog attributes and fields may contain data of one of the following types.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9af44474-0512-452a-af9e-48918e9da6ca
TQID: 'https://experienceleague.adobe.com/bf3PkSBKhuIzaRglWXs6UH0RoikSPcRUZBIAFdOaHV0'
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
