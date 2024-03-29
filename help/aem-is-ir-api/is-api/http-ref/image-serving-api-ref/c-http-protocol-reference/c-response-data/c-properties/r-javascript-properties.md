---
title: JavaScript properties
description: If JavaScript is specified as the response format, the reply data is formatted so that it is parsed as a JavaScript&trade; include file.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 12e69221-4a2c-4ec6-b38b-0a8d98d3c4a6
---
# JavaScript properties{#javascript-properties}

If JavaScript is specified as the response format, the reply data is formatted so that it is parsed as a JavaScript include file.

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

The *`propertyValue`* can be empty. White space is optional at the beginning and end of each line and before and after the = separator. All values are enclosed by single quotes. Single quotes in strings are escaped with two consecutive single quotes.

To parse a JavaScript properties response, any object or objects referenced in the response must be created before the properties file is loaded. Following is an example for using `req=props` to obtain the response image size in JavaScript:

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```
