---
description: Substitution variables are used to transfer values from the request URL to compositing templates stored in image catalogs. Variables can also be used to convey the same value to different places in a complex request.
seo-description: Substitution variables are used to transfer values from the request URL to compositing templates stored in image catalogs. Variables can also be used to convey the same value to different places in a complex request.
seo-title: Substitution variables
solution: Experience Manager
title: Substitution variables
uuid: e369f2c3-8d89-4169-8869-f1d7ab89aab9
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Business Practitioner"
---

# Substitution variables{#substitution-variables}

Substitution variables are used to transfer values from the request URL to compositing templates stored in image catalogs. Variables can also be used to convey the same value to different places in a complex request.

 ` $ *`var`*= *`value`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>Variable name. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
  <td class="stentry"> <p>Value to which the variable is to be set (string). </p> </td> 
 </tr> 
</table>

Variable definitions and references may occur in the query portion of the request, in `catalog::Modifier`, and in `catalog::PostModifier`.

Variables are defined as above, similar to other IS commands; the leading '$' identifies the command as a variable definition. Variables must be defined before they are referenced.

The variable name *`var`* is not case-sensitive and may consist of any combination of ASCII letters, numbers, '-', '_', and '.'.

>[!NOTE]
>
>*`value`* must be single-pass URL-encoded for safe HTTP transmission. Double-encoding is required if *`value`* is retransmitted via HTTP. This is the case when *`value`* is substituted into a nested foreign request or into the href attribute of an SVG `<image>` element.

Variable references consist of the variable name delimited by leading and trailing '$' ($*var*$). References may occur anywhere in the value portion of any IS commands (i.e. between the '=' following the command name and the subsequent '&' or the end of the request). Custom variables cannot be applied to the `layer=` and `effect=` commands. Multiple variables are permitted in the same command value. The server substitutes each occurrence of ` $ *`var`*$` with *`value`*.

Variable references may not be nested. Any occurrences of ` $ *`var`*$` within *`value`* are not substituted.

For example, the request fragment:

`$var2=apple&$var1=my$var2$tree&text=$var1$`

resolves to:

`text=my$var2$tree`

>[!NOTE]
>
>'$' is not a reserved character; it may occur otherwise in the request. For example, `src=my$image$file.tif` is a valid command (assuming that a catalog entry or image file named `my$image$file.tif` exists), while `wid=$number$` is not, because `wid` requires a numeric argument.

## Variable processing in nested requests {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`var`*$` references may occur anywhere within the curly braces of a nested Image Serving or Image Rendering request, including to the left of the '?' separating the path from the query. The server substitutes these references with values (either from the url or from `catalog::Modifier` of the main image catalog) before further parsing and processing of the nested request.

In addition, all ` $ *`var`*=` definitions from the url or `catalog::Modifier` are forwarded to all nested Image Serving and Image Rendering requests. This ensures that all variable definitions are available to all templates, regardless of nesting level.

Regardless of the nesting level, only single-pass HTTP-encoding must be applied to variable values which are to be substituted anywhere in nested Image Rendering or Image Serving requests or their associated `catalog::Modifier` strings.

## Variable processing in embedded foreign requests {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`var`*$` references occurring anywhere within the curly braces of an embedded foreign request are substituted with matching variable definition values. This allows embedded foreign requests to be placed in a template in an image catalog.

Variable values which are to be substituted into foreign requests typically must be double-encoded, since no re-encoding is applied before the server attempts to transmit the final foreign url.

## Variable processing in SVG files {#section-a8359f9909764142b6a18ae778dca913}

` $ *`var`*$` references may occur in SVG files in attribute values and in `<text>` strings. Image Serving substitutes these with the matching ` $ *`var`*=` definitions known at the request nesting level at which the SVG file is specified.

>[!NOTE]
>
>Any variable value which is to be substituted into an `href` attribute value must be double URL-encoded; all others must be singly encoded.

## Pre-defined path variable {#section-930d0dd12e8f49499becc9fe8df24092}

The *`object`* specified in the request path is assigned to the pre-defined variable `*`$object`*`. ' ` $ *`object`*$`' may be placed anywhere in the request, in the template referenced by the request, or in a nested/embedded request where such object is permitted, including the value of `src=` and `mask=`, and the path of a nested/embedded request.

For example, the following request will reuse the image specified in the path as the source of a layer in a nested request:

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

This is equivalent to

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

The definition of `*`$object`*` can be overridden by explicitly specifying ` $ *`object`*=` with the desired value.

The predefined path variable is commonly used in conjunction with `template=`.

## Default {#section-b02483d15529444586a2e9504805b155}

None. Only variables which have been defined will be substituted by the server (except the pre-defined path variable $object, which will always be substituted). Any occurrences of ` $ *`var`*$` remain literal if `*`var`*`cannot be matched with an existing variable definition.

## Examples {#section-fba9393df6984247b7e30b3f93992e86}

See "Example A" in [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## See also {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14) 
