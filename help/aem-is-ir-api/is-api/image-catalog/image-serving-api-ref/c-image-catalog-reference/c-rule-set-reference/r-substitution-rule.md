---
description: Substitution string element. Optional in <rule> elements.
solution: Experience Manager
title: substitution
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0f1c558-b745-41dc-bf65-1bf1fdcb88d3
---
# substitution{#substitution}

Substitution string element. Optional in `<rule>` elements.

## Attributes {#section-a4506fcb765f4f128f7f1f2629b18a6c}

None.

## Data {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

Substitution string.

## Description {#section-4a64a93f5e1a4d04a2db19166578bf76}

Defines a replacement string for the matched string or substring in the path or query.

If the pattern expression includes sub-expressions (delimited with parentheses), the first matched substring is replaced with the substitution string. If the pattern expression does not include sub-expressions, the entire matched string is substituted.

If `<expression>` is empty or absent, the substitution string is appended to the path or query.

If `<substitution>` is empty, the matched string or substring is removed. If `<substitution>` is not specified, the path or query string is not modified.

>[!NOTE]
>
>All matches in the input string are substituted when `replace="all"` is specified in the `<rule>`,element to which this `<substitution>` element belongs. By default, only the first match is replaced with the substitution string.

## Note {#section-cedf2adabaaf441c9f598fb0ea180246}

The substitution string must not contain literal < and & characters. These reserved characters can be encoded with `&` and `<`, respectively, or the entire string can be enclosed in an XML CDATA section:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
