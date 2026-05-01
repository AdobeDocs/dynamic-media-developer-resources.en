---
title: JavaScript properties
description: If JavaScript is specified as the response format, the reply data is formatted so that it is parsed as a JavaScript&trade; include file.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 12e69221-4a2c-4ec6-b38b-0a8d98d3c4a6
TQID: https://experienceleague.adobe.com/EtjCH-gjC9f6e13yjALZfP1yoMkT7ONMrobAVC2Id-s
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
