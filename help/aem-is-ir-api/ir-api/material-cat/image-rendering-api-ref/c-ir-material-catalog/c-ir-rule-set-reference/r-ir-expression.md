---
description: Regular-expression pattern element. Optional in <rule> elements.
solution: Experience Manager
title: expression
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 5fb95e93-cf14-4042-a338-d9d7df6e3b58
---
# expression{#expression}

Regular-expression pattern element. Optional in `<rule>` elements.

## Attributes {#section-fd0574eee1f9423cbb2ed709c0906800}

None.

## Data {#section-4cd740c511a1432da0955e9acfbcf96f}

Regular-expression pattern string.

## Description {#section-3245c8a531bb455d8398449f6ea63b37}

The `<expression>` element can be empty or contain a simple search string or a regular-expression pattern. The pattern is applied to the entire request string.

A match always occurs when `<expression>` is empty or not specified; this is equivalent to specifying `<expression>.*</expression>`.

The implementation is based on the Java package [java.util.regex](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e), which provides a regular-expression syntax similar to Perl's.

## Note {#section-6b41a900b0ce4a9590e5861e3c81599c}

The expression string must not contain literal < and & characters. These reserved characters can be encoded with `&` and `<`, respectively, or the entire string can be enclosed in an XML `CDATA` section:

`<expression><![CDATA[&fmt=custom]]></expression>`

All characters between the `<expression>` and `</expression>` tags are passed to the regular expression parser, including characters outside the optional `CDATA` section. Care should be taken to avoid extra whitespace.

## See also {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
