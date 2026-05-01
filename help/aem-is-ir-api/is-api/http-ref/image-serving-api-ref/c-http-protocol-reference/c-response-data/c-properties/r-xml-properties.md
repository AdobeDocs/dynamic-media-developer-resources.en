---
description: If xml is specified as the response format, the reply data is formatted as an XML document which can be parsed by any standard XML parser.
solution: Experience Manager
title: XML properties
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84cae0cd-d13b-409e-bd65-71c7e973d4b8
TQID: https://experienceleague.adobe.com/3My3hFrzr2MakxEzgNOm2rVJN6vzLUDE92lax5eiieI
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
# XML properties{#xml-properties}

If xml is specified as the response format, the reply data is formatted as an XML document which can be parsed by any standard XML parser.

 A typical properties response document has this general structure:

```
<?xml version="1.0" encoding="UTF-8" ?>
<prop-group>
   <prop-group name="
<varname>
  objectName
</varname>">
       <property name="
<varname>
  propertyName
</varname>" value="
<varname>
  propertyValue
</varname>" />
       ...
    </prop-group>
 ...
</prop-group>

```

The `<prop-group>` element is used as the outermost container, and for grouping properties. If a group is named, the name corresponds to the Java/JavaScript object name.

>[!NOTE]
>
>Character encoding may be specified for some `req=` types. Refer to the description of the specific `req=`command for details.
