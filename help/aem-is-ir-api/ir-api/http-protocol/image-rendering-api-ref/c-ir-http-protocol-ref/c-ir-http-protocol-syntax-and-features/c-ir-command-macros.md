---
title: Command macros
description: Command macros provide named shortcuts for sets of commands.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 00f6d27e-9f6b-4eea-8f42-833fbc0f1c38
TQID: https://experienceleague.adobe.com/4ZS4QGYvxRGqaVJ-OtE4gIa292JLToYxvEcgzk4PUkI
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
# Command macros{#command-macros}

Command macros provide named shortcuts for sets of commands.

 `$ *[!DNL name]*$`

** *[!DNL name]* ** Macro name

Macros are defined in separate macro definition files, which can be attached to material catalogs or the default catalog.

*[!DNL name]* is not case-sensitive and can consist of any combination of ASCII letters, numbers , '-', '_', and '.' characters.

Invoke macros anywhere in a request after the '?', or anywhere within a `vignette::Modifier` field. Macros can only represent one or more Image Rendering commands and must be separated from other commands with '&' separators.

Macro invocations are replaced by their substitution strings early during parsing. Commands within macros override the same commands in the request if they occur before the macro invocation in the request. This workflow is different from `vignette::Modifier`, where commands in the request string override commands in the `vignette::Modifier` string, regardless of the position in the request.

Command macros cannot have argument values, but custom variables may be used to pass values from the request into the macro.

Macros may not be nested.

**Example**

Macros can be useful if the same commands or attributes are to be applied to different rendered images.

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

You can define a macro for the common attributes:

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

The macro would be used as follows:

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

Because `qlt=` is different for the third request, the software overrides the value after the macro is invoked (specifying `qlt=` *before* `$render$`is ineffective).

**See also**

`catalog::MacroFile`, `catalog::Modifier`, Macro Definition Reference

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->
