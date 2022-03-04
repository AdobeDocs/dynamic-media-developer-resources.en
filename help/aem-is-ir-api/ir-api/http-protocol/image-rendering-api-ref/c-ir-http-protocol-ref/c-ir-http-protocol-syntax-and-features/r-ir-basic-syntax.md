---
title: Image Rendering HTTP protocol basic syntax
description: This section describes the basic syntax of the Dynamic Media Image Rendering HTTP protocol.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8bf5920a-7ada-4db5-9796-05c5a17532c8
---
# Image Rendering HTTP protocol basic syntax{#image-rendering-http-protocol-basic-syntax}

This section describes the basic syntax of the Dynamic Media Image Rendering HTTP protocol.

<table id="table_0A7D7207EE6D4B08B62BE8620EBE0B25"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Item </p> </th> 
   <th colname="col2" class="entry"> <p>Definition </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> request</span> </p> </td> 
   <td colname="col2"> <p>http://<span class="varname"> server</span>/ir/render[/<span class="varname"> vignette</span> ] [ ?<span class="varname"> modifiers</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> server </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> server_address</span> [ :<span class="varname"> port</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> vignette </span> </p> </td> 
   <td colname="col2"> <p>Vignette specifier (relative file path or vignette catalog entry). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modifiers </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> modifier</span> *[ &amp; <span class="varname"> modifier</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modifier </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> command</span> | { $ <span class="varname"> macro</span> $ } | { .<span class="varname"> comment</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> command </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } } [ = <span class="varname"> value</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> macro </span> </p> </td> 
   <td colname="col2"> <p>Name of a command macro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> comment </span> </p> </td> 
   <td colname="col2"> <p>Comment string (ignored by server). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> cmdName </span> </p> </td> 
   <td colname="col2"> <p>Name of a command or attribute. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> var </span> </p> </td> 
   <td colname="col2"> <p>Name of a custom variable. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> value </span> </p> </td> 
   <td colname="col2"> <p>Command or variable value. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*, *`cmdName`*, *`macro`*, and *`var`* are case-insensitive. The server preserves the case of all other string values.

**Server identifier**

The ' `/ir/render`' root context is required for all HTTP requests to Image Rendering.

**Comments**

Comments may be embedded into request strings anywhere and are identified by a period (.) immediately following the command separator (&). The comment is terminated by the next occurrence of an (unencoded) command separator. This feature may be used to add information to the request which is not for Image Serving use, such as time stamps, and database ids.

**HTTP decoding**

Image Rendering first extracts *`object`* and *`modifiers`* from the incoming request. The *`object`* is then separated into path elements which are individually HTTP-decoded. The *`modifiers`* string is separated into *`command`*= *`value`* pairs, and *`value`* is then HTTP-decoded before command-specific processing.
