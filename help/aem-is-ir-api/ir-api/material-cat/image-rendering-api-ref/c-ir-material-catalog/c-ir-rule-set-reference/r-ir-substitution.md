---
title: substitution
description: Substitution string element. Optional in <rule> elements.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea44d940-e8dd-4a25-a082-3ed3c0f57e45
TQID: 'https://experienceleague.adobe.com/GqJBLso7oigoeCJ-0KQzFv2aeoAiVzumjlDTtjBSDI4'
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
# substitution{#substitution}

Substitution string element. Optional in `<rule>` elements.

## Attributes {#section-d955eefc53eb4274861270669c01f9ca}

None.

## Data {#section-a2688866ed6d41279a8478886e511ae3}

Substitution string.

## Description {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

Defines a replacement string for the matched string or substring in the path or query.

If the pattern expression includes subexpressions (delimited with parentheses), the first matched substring is replaced with the substitution string. If the pattern expression does not include subexpressions, the entire matched string is substituted.

If `<expression>` is empty or absent, the substitution string is appended to the path or query.

If `<substitution>` is empty, the matched string or substring is removed. If `<substitution>` is not specified, the path or query string is not modified.

## Note {#section-90fe89bb17a04804b7ff3c93df082892}

The substitution string must not contain literal < and & characters. These reserved characters can be encoded with `&` and `<`, respectively, or the entire string can be enclosed in an XML `CDATA` section:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
