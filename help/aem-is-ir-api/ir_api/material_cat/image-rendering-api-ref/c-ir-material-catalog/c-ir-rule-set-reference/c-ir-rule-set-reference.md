---
description: Image Rendering supports a simple request pre-processing mechanism which is based on regular-expression match and substitution rules.
seo-description: Image Rendering supports a simple request pre-processing mechanism which is based on regular-expression match and substitution rules.
seo-title: Rule set reference
solution: Experience Manager
title: Rule set reference
topic: Scene7 Image Serving - Image Rendering API
uuid: 265d69ae-57c7-4c2c-814a-679e955c0e4d
index: y
internal: n
snippet: y
---

# Rule set reference{#rule-set-reference}

Image Rendering supports a simple request pre-processing mechanism which is based on regular-expression match and substitution rules.

<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>

Collections of pre-processing rules (*rule sets*) can be attached to material catalogs or the default catalog. Rules in the default catalog apply only if the request does not attach a specific material catalog.

Request pre-processing rules can modify the path and query portions of requests before they are processed by the server's request parser, including manipulating the path, adding commands, changing command values, and applying templates or macros. Rules can also be used to configure and override some catalog attributes, as well as for limiting service to specific client IP addresses.

Rule sets are stored as XML document files. The relative or absolute path of the rule set file must be specified in `attribute::RuleSetFile`.

## General structure {#section-74faaee27fc543a2ab4a306f3a03674e}

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE ruleset SYSTEM" RuleSet.dtd">
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
   </rule>
</ruleset>
```

The `<?xml>`, `<!DOCTYPE>` and `<ruleset>` elements are always required in a valid rule set XML file, even if no actual rules are defined.

One `<ruleset>` element containing any number of `<rule>` elements are permitted.

Contents of preprocessing rule files are case-sensitive.

## URL pre-processing {#section-737a38d1b8c746f995e64fa6cfbcec87}

Before any other processing, an incoming HTTP request is partially parsed to determine which material catalog should be applied. Once the catalog is identified, the rule set for the selected catalog (or the default catalog, if no specific catalog was identified) is applied.

The `<rule>` elements are searched in the order specified for a match with the contents of the `<expression>` element ( *`expression`*).

If a `<rule>` is matched, the optional *`substitution`* is applied and the modified request string is passed to the server's request parser for normal processing.

If no successful match is made when the end of the <ruleset> is reached, the request is passed to the parser without modification.

## The OnMatch attribute {#section-7a8ad3597780486985af5e9a3b1c7b56}

The default behavior can be modified with the `OnMatch` attribute of the `<rule>` elements. `OnMatch` may be set to `break` (default), `continue`, or `error.`

<table id="table_4CABF55B33854A128D5F326B31C6C397"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Element and attribute </p> </th> 
   <th colname="col2" class="entry"> <p>Behavior when a match occurs </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="break"&gt;</span> </p> </td> 
   <td colname="col2"> <p>Rule processing is terminated immediately after the substitution for this rule has been applied. Default. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="continue"&gt;</span> </p> </td> 
   <td colname="col2"> <p>The substitution is applied and processing continues with the next rule. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="error"&gt;</span> </p> </td> 
   <td colname="col2"> <p>Rule processing is terminated immediately and a "request refused" response status is returned to the client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Overriding catalog attributes {#section-1f59ce84234f4576ba8473b0e6ba22ee}

`<rule>` elements may optionally define attributes that override the corresponding catalog attributes when the rule is successfully matched and `OnMatch="break"` is set. No attributes are applied if `OnMatch="continue"` is set. Refer to the description of `<rule>` for a list of attributes that can be controlled with rules.

## Regular expressions {#section-4d326507b52544b0960a9a5f303e3fe6}

Simple string matching works for very basic applications, but regular expressions are required in most instances. While regular expressions are industry-standard, the specific implementation varies from instance to instance.

[package java.util.regex](http://docs.oracle.com/javase/1.4.2/docs/api/java/util/regex/package-summary.html) describes the specific regular expression implementation used by Image Serving.

## Captured substrings {#section-8057cd65d48949ffb6a50e929bd3688b}

To facilitate complex URL modifications, substrings may be captured in the expression by enclosing the substring with parentheses (…). Captured substrings are numbered sequentially starting with 1 according to the position of the leading parenthesis. The captured substrings may be inserted in the substitution using *`$n`*, where *`n`* is the sequence number of the captured substring.

## Managing rule set files {#section-e8ce976b56404c009496426fd334d23d}

One rule set file can be attached to each material catalog with the catalog attribute `attribute::RuleSetFile`. While you can edit the rule set file at any time, the image server recognizes the changes only when the associated material catalog is reloaded. This happens when the Platform Server is started or restarted and whenever the primary catalog file (which has a [!DNL .ini] file suffix) is modified or 'touched' (to change the file date).

## Examples {#section-c4142a41f5cd4ff799a72fbc130c3700}

Ruleset examples are provided in the corresponding section of the Image Catalog Reference in the Image Serving documentation.

## See also {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[package java.util.regex](http://docs.oracle.com/javase/1.4.2/docs/api/java/util/regex/package-summary.html) 
