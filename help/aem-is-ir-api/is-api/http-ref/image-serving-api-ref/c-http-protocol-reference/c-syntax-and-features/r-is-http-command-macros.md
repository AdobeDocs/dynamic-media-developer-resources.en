---
description: Command macros provide named shortcuts for sets of commands. Macros are defined in separate macro definition files, which can be attached to image catalogs or the default catalog.
seo-description: Command macros provide named shortcuts for sets of commands. Macros are defined in separate macro definition files, which can be attached to image catalogs or the default catalog.
seo-title: Command macros
solution: Experience Manager
title: Command macros
topic: Scene7 Image Serving - Image Rendering API
uuid: a6ff5642-6716-484f-b37e-066994362a9b
---

# Command macros{#command-macros}

Command macros provide named shortcuts for sets of commands. Macros are defined in separate macro definition files, which can be attached to image catalogs or the default catalog.

 `$ *`name`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> name</span></span> </p> </td> 
  <td class="stentry"> <p>Macro name. </p></td> 
 </tr> 
</table>

` *`name`*` is not case-sensitive and may consist of any combination of ASCII letters, numbers , '-', '_', and '.' characters.

Macros may be invoked anywhere in a request after the '?', as well as anywhere within a `catalog::Modifier` or `catalog::PostModifier` field. Macros can only represent one or more complete Image Serving commands and must be separated from other commands with '&' separators.

Macro invocations are replaced by their substitution strings early during parsing. Commands within macros will override the same commands in the request if they occur before the macro invocation in the request. This is different from `catalog::Modifier`, where commands in the request string will always override commands in the `catalog::Modifier` string, regardless of position in the request.

Command macros cannot have argument values, but custom variables may be used to pass values from the request into the macro.

Macros may be nested, with the following restriction: A macro can only be invoked if it is already defined at the time the macro definition is parsed, either by appearing earlier in the same macro definition file, or by placing the definition for such an embedded macro in the default macro definition file.

## Example {#section-2f73d36ac8d64254a03bae5afeae2fb9}

Macros can be useful if the same attributes are to be applied to different images.

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

We can define a macro for the common attributes:

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

The macro would be used as follows:

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

Since `wid=` is different for the third request, we simply override the value *after* the macro is invoked (specifying `wid=`*before* `$view$` would not have any effect).

## See also {#section-8cdba0ed2480444ca61e719e54f8871c}

[catalog::MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) , [catalog::Modifier](r_modifier_cat.md#reference_D2C6884B3A2248FAB81A112D27969834), [Macro Definition Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79) 
