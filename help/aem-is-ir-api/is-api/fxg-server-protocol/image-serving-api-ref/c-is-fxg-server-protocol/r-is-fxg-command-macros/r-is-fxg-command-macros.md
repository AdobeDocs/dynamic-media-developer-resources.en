---
title: Command macros
description: Command macros provide named shortcuts for sets of commands.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc149977-3ca8-4612-ad05-4d565440d00a
TQID: 'https://experienceleague.adobe.com/DbXn35KC7OLFI0Dulgobj3UFPHnubmCisNDS541j8lE'
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

Macros are defined in separate macro definition files, which can be attached to image catalogs or the default catalog.

Macros may be invoked anywhere in a request after the '?', and anywhere within a `catalog::Modifier` field. Macros can only represent one or more full Image Serving commands, therefore it must be enclosed by '&' separators (except when at the beginning or end of the modifier string).

Macro invocations are replaced by their substitution strings early during parsing. Commands within macros override the same commands in the request if they occur before the macro invocation in the request. This flow is different from `catalog::Modifier`, where commands in the request string always override commands in the `catalog::Modifier` string, regardless of the position in the request.

Macros can be nested. However, a macro can only be invoked if it is already defined at the time the macro definition is parsed. This flow is accomplished either by appearing earlier in the same macro definition file, or by placing the definition for such an embedded macro in the default macro definition file.

Macros can be useful if the same attributes are to be applied to different images.

[!DNL `http://server/cat/1345?wid=240&fmt=pdf&imageRes=300`]

[!DNL `http://server/cat/1435?wid=240&fmt=pdf&imageRes=300`]

[!DNL `http://server/cat/8243?wid=480&fmt=pdf&imageRes=300`]

You can define a macro for the common attributes:

`view wid=240&fmt=pdf&imageRes=300`

The macro would be used as follows:

[!DNL `http://server/cat/1345?$view$`]

[!DNL `http://server/cat/1435?$view$`]

[!DNL `http://server/cat/8243?$view$&wid=480`]

Because `wid=` is different for the third request, you simply override the value *after* the macro is invoked (specifying `wid=` *before* `$view$` has no effect). 

+ [name](r-name.md)
