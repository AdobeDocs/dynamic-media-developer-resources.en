---
description: If text is specified as the response format, the reply data is formatted to be readable as Java properties.
solution: Experience Manager
title: Text (Java) properties
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f5dbc8-fbdc-4204-a6a0-60f34378c3e1
TQID: https://experienceleague.adobe.com/ooogJuWAnwUnyvlWupgzCjumOt7eUINpp0hSaATdtnk
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
