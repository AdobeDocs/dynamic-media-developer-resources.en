---
description: Substitution string element. Optional in <rule> elements.
seo-description: Substitution string element. Optional in <rule> elements.
seo-title: substitution
solution: Experience Manager
title: substitution
topic: Scene7 Image Serving - Image Rendering API
uuid: 5609dd95-b6f0-4e4f-99cf-90b979418922
index: y
internal: n
snippet: y
---

# substitution{#substitution}

Substitution string element. Optional in <rule> elements.

## Attributes {#section-d955eefc53eb4274861270669c01f9ca}

None.

## Data {#section-a2688866ed6d41279a8478886e511ae3}

Substitution string.

## Description {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

Defines a replacement string for the matched string or sub-string in the path or query.

If the pattern expression includes sub-expressions (delimited with parentheses), the first matched sub-string is replaced with the substitution string. If the pattern expression does not include sub-expressions, the entire matched string is substituted.

If `<expression>` is empty or absent, the substitution string is appended to the path or query.

If `<substitution>` is empty, the matched string or sub-string is removed. If `<substitution>` is not specified, the path or query string is not modified.

## Note {#section-90fe89bb17a04804b7ff3c93df082892}

The substitution string must not contain literal < and & characters. These reserved characters can be encoded with `&` and `<`, respectively, or the entire string can be enclosed in an XML `CDATA` section:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>` 
