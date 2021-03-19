---
description: If javascript is specified as the response format, the reply data is formatted to be parsed as a JavaScript include file.
seo-description: If javascript is specified as the response format, the reply data is formatted to be parsed as a JavaScript include file.
seo-title: JavaScript properties
solution: Experience Manager
title: JavaScript properties
uuid: 832a927e-ecaf-438c-8fbf-a702d58902d8
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Business Practitioner"
---

# JavaScript properties{#javascript-properties}

If javascript is specified as the response format, the reply data is formatted to be parsed as a JavaScript include file.

A typical JavaScript properties response has this general structure:

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`* may be empty. White space is optional at the beginning and end of each line and before and after the = separator. All values are enclosed by single quotes. Single quotes in strings are escaped with two consecutive single quotes.

To parse a JavaScript properties response, any object(s) referenced in the response must be created before the properties file is loaded. Following is an example for using `req=props` to obtain the response image size in JavaScript:

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```

