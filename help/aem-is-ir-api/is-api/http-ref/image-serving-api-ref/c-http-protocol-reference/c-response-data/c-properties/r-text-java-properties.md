---
description: If text is specified as the response format, the reply data is formatted to be readable as Java properties.
solution: Experience Manager
title: Text (Java) properties
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f5dbc8-fbdc-4204-a6a0-60f34378c3e1
---
# Text (Java) properties{#text-java-properties}

If text is specified as the response format, the reply data is formatted to be readable as Java properties.

A typical text properties response has this general structure:

```
#S7Z OK
#
<varname>
  timeStamp
</varname>
<varname>
  objectName.propertyName
</varname>=
<varname>
  propertyValue
</varname>
...
```

*`propertyValue`* may be empty. White space is optional at the beginning and end of each line and before and after the = separator. Single or double quotes may be used to enclose string values, but are not required.

String values may contain JAVA-style escape characters, such as `\n`, `\t`, `\:`, or `\\`.
