---
title: Custom variables
description: The query portion of requests and vignette Modifier strings may include user-defined variables.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8d26b797-5099-49fb-b7e0-46747f35ab84
---
# Custom variables{#custom-variables}

The query portion of requests and vignette::Modifier strings may include user-defined variables.

 `$ [!DNL name] = [!DNL value]`

`[!DNL name]` - Variable name. May consist of any combination of alpha, digit, and safe characters, excluding `$`.

`[!DNL value]` - Value to which the variable is to be set (string).

Variables are defined similar to other server commands, using the above syntax. Variables must be defined before they can be referenced. Variables which are defined in `vignette::Modifier` can be referenced in the URL request, and conversely.

>[!NOTE]
>
>`[!DNL value]` must be single-pass URL-encoded for safe HTTP transmission. Double encoding is required if `[!DNL value]` is retransmitted by way of HTTP. This situation is the case when `[!DNL value]` is substituted into a nested foreign request.

Variables are referenced by embedding the variable name (enclosed by a leading and a trailing `$`) anywhere in command values. For example, between the `=`  following the command name and the subsequent `&` or the end of the request. The server substitutes each such occurrence of `$ [!DNL name]$` with `[!DNL string]`. No substitutions happen on any occurrences of `$ [!DNL name]$` in command names (before the equal sign of a command), and in the path portion of the request.

Custom variables may not be nested. Any occurrences of `$ [!DNL name]$` within `[!DNL string]` are not substituted. For example, the request fragment `$var2=apple&$var1=my$var2$tree&text=$var1$` resolves to `text=my$var2$tree`.

`$` is not a reserved character; it may occur otherwise in the request. For example, `src=my$texture$file.tif` is a valid command (assuming that a material catalog entry or texture file named `[!DNL my$texture$file.tif]` exists), while `wid=$number$` is not, because `wid=` requires a numeric argument.
