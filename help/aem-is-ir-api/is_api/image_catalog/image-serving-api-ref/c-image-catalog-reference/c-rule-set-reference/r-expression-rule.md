---
description: Regular expression pattern element. Optional in <rule> elements.
seo-description: Regular expression pattern element. Optional in <rule> elements.
seo-title: expression
solution: Experience Manager
title: expression
topic: Scene7 Image Serving - Image Rendering API
uuid: 8a654d26-3961-48a7-903b-9569ee8c093f
index: y
internal: n
snippet: y
---

# expression{#expression}

Regular expression pattern element. Optional in <rule> elements.

## Attributes {#section-2d438c889ae84b6da7e0ed84b5d021a0}

None.

## Data {#section-e2601008d71243109af1a8c55b58416d}

Regular-expression pattern string.

## Description {#section-759bfb738ddb45dba1f0807aba8c1113}

The `<expression>` element can be empty or contain a simple search string or a regular-expression pattern. The pattern is applied to the entire request string.

A match always occurs when `<expression>` is empty or not specified; this is equivalent to specifying `<expression>.*</expression>`.

The implementation is based on the Java package [java.util.regex](http://docs.oracle.com/javase/1.4.2/docs/api/java/util/regex/package-summary.html), which provides regular expression syntax similar to Perl's.

## Notes {#section-10b472a902674893b49ca49a7052c366}

The expression string must not contain literal < and & characters. These reserved characters can be encoded with `&` and `<`, respectively, or the entire string can be enclosed in an XML `CDATA` section:

`<expression><![CDATA[&fmt=custom]]></expression>`

All characters between the `<expression>` and `</expression>` tags are passed to the regular expression parser, including characters outside the optional `CDATA` section. Care should be taken to avoid extra whitespace.

## See also {#section-ca98548917d945f4b71f18208f0e6840}

[java.util.regex](http://docs.oracle.com/javase/1.4.2/docs/api/java/util/regex/package-summary.html) 
