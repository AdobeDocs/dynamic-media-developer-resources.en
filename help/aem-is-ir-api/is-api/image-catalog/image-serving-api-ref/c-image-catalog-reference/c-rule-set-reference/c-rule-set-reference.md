---
description: Image Serving supports a simple request preprocessing mechanism which is based on regular-expression match and substitution rules.
seo-description: Image Serving supports a simple request preprocessing mechanism which is based on regular-expression match and substitution rules.
seo-title: Rule set reference
solution: Experience Manager
title: Rule set reference
topic: Scene7 Image Serving - Image Rendering API
uuid: 356e4939-c57d-459a-8e40-9b25e20fc0a3
---

# Rule set reference{#rule-set-reference}

Image Serving supports a simple request preprocessing mechanism which is based on regular-expression match and substitution rules.

 Collections of pre-processing rules (*rule sets*) can be attached to image catalogs or the default catalog. Rules in the default catalog apply only if the request does not identify a specific main image catalog.

Request pre-processing rules can modify the path and query portions of requests before they are processed by the Platform Server's parser, including manipulating the path, adding commands, changing command values, and applying templates or macros. Rules can also be used to configure and override certain security features which are normally controlled only with catalog attributes, such as request obfuscation, water-marking, as well as limiting service to specific client IP addresses.

Rule sets are stored as XML document files. The relative or absolute path of the rule set file must be specified in `attribute::RuleSetFile`.

## General structure {#section-8bcbd91ea8a946f28051bde8ad21827f}

```
 <?xml version="1.0" encoding="UTF-8"?> 
<ruleset> 
   <rule> 
      <expression> 
<varname>
  expression 
</varname></expression> 
      <substitution> 
<varname>
  substitution 
</varname></substitution> 
      <addressfilter> 
<varname>
  addressFilter 
</varname></addressfilter> 
      <header> 
<varname>
  headerValue 
</varname></header>  
   </rule> 
</ruleset>
```

The `<?xml>` and `<ruleset>` elements are always required in a valid rule set XML file, even if no actual rules are defined.

One `<ruleset>` element containing any number of `<rule>` elements are permitted.

The contents of preprocessing rule files are case-sensitive.

## Ruleset validation {#section-d8d101a0b4d74580835e37d128d05567}

A copy of [!DNL RuleSet.xsd] is provided in the catalog folder and should be used to validate a ruleset file before registering it in the [!DNL catalog.ini] file. Note that Image Serving uses an internal copy of [!DNL RuleSet.xsd] for validation.

## URL pre-processing {#section-2c09a2d79ada46b994857c6a7fb4c13a}

Before any other processing, an incoming HTTP request is partially parsed to determine which image catalog should be applied. Once the catalog is identified, the rule set for the selected catalog (or the default catalog, if no specific catalog was identified) is applied.

The `<rule>` elements are searched in the order specified for a match with the contents of the `<expression>` element ( *`expression`*).

If a `<rule>` is matched, the optional *`substitution`* is applied and the modified request string is passed to the server's request parser for normal processing.

If no successful match is made when the end of the `<ruleset>` is reached, the request is passed to the parser without modification.

## The OnMatch attribute {#section-ed952fa55d99422db0ee68a2b9d395d3}

The default behavior can be modified with the `OnMatch` attribute of the `<rule>` element. `OnMatch` may be set to `break` (default), `continue`, or `error`. 

<table id="table_6680A81492B24CE593330DA7B0075E8F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Element and Attribute</b> </th> 
   <th class="entry"> <b>Behavior when a match occurs</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="break"&gt; </span> </p> </td> 
   <td> <p>Rule processing is terminated immediately after the substitution for this rule has been applied. Default. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="continue"&gt; </span> </p> </td> 
   <td> <p>The substitution is applied and processing continues with the next rule. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="error"&gt; </span> </p> </td> 
   <td> <p>Rule processing is terminated immediately and a "request refused" response status is returned to the client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Overriding catalog attributes {#section-3f1e33a65c5346d1b4a69958c61432f3}

`<rule>` elements can optionally define attributes that override the corresponding catalog attributes when the rule is successfully matched. If multiple matched rules set the same attribute, the last one prevails. Refer to the description of the ` [<rule>](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md#reference-af76c0e2b8be48dabb52b71fe7e51ee9)` element for a list of attributes that can be controlled with rules.

## Regular expressions {#section-3f77bb9a265147b38c645f63ab1bad8b}

Simple string matching works for very basic applications, but regular expressions are required in most instances. While regular expressions are industry-standard, the specific implementation varies from instance to instance.

[ [!DNL package java.util.regex] ](http://docs.oracle.com/javase/1.4.2/docs/api/java/util/regex/package-summary.html) describes the specific regular expression implementation used by Image Serving.

## Captured substrings {#section-066e659406d5403599cd26ae35e80d68}

To facilitate complex URL modifications, substrings may be captured in the expression by enclosing the substring with parentheses (…). Captured substrings are numbered sequentially starting with 1 according to the position of the leading parenthesis. The captured substrings may be inserted in the substitution using ` $ *`n`*`, where *`n`* is the sequence number of the captured substring.

## Managing rule set files {#section-0598a608e4044bb4805fe93ceebe10a9}

One rule set file can be attached to each image catalog with the catalog attribute `attribute::RuleSetFile`. While you can edit the rule set file any time, the image server recognizes the changes only when the associated image catalog is reloaded. This reloading happens when the platform server is started or restarted and whenever the primary catalog file, which has an [!DNL .ini] file suffix, is modified or "touched" to change the file date.

## Examples {#section-aa769437d967459299b83a4bf34fe924}

**Example A.** Define a rule that increases the image quality settings if the image name has the suffix " [!DNL _hg]":

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

The rule expression specifies a case-insensitive match of " [!DNL _hg]" at the end of the URL string. The suffix is replaced with the specified query string which changes the image quality settings. Note that the `?` character in the substitution string is escaped since this is a special character in regular expressions.

>[!NOTE]
>
>The required encoding for the ampersand character. Alternatively, the substitution string could be enclosed in a CDATA block:

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**Example B.** A particular web application does not permit query strings. Define a rule which translates the trailing path element `small`, `medium`, or `large` to a template, using the remainder of the path as the image name. For example, `myCat/myImage/small` would translate to `myCat/smallTemplate?src=myCat/myImage`.

We can use substrings to restructure the request:

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## See also {#section-9b748e7c5cff4759a70f96657bd43352}

[package java.util.regex](http://docs.oracle.com/javase/1.4.2/docs/api/java/util/regex/package-summary.html) 
