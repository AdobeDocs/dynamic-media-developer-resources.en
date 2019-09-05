---
description: If xml is specified as the response format, the reply data is formatted as an XML document which can be parsed by any standard XML parser.
seo-description: If xml is specified as the response format, the reply data is formatted as an XML document which can be parsed by any standard XML parser.
seo-title: XML properties
solution: Experience Manager
title: XML properties
topic: Scene7 Image Serving - Image Rendering API
uuid: 9f78f9b2-c329-49e3-b822-c6d3f8c9908c
index: y
internal: n
snippet: y
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

