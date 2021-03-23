---
description: Request type. Specifies the type of request.


solution: Experience Manager
title: req

feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# req{#req}

Request type. Specifies the type of request.

 `req={validate|contents|oversetstatus|exists}`

<table id="table_F39239E5244746DB9F253BB0D5E85D54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Value </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> validate</span> </p> </td> 
   <td colname="col2"> <p> Returns any errors with rendering the fxg with the provided url modifiers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> contents</span> </p> </td> 
   <td colname="col2"> <p> Return xml list of all elements with a <span class="codeph"> s7:element</span> attribute value and a list of all pages in the fxg document. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>Returns XML list of which <span class="codeph"> &lt;RichText/&gt;</span> elements are overset. </p> <p>Returns an xml list of <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> elements that are overset for processing on the client side. Only <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> elements that are overset will be returned. <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> is a required <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> attribute when using <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>. Any overset <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> elements without a <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> is not listed. Each <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> element in the list has the <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>, <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>, and the bounding box of the overset text frame. The <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> attribute indicates the text index in the story up to which text was able to fit in the frame. <span class="+ topic/ph pr-d/codeph codeph"> Req=oversetstatus</span> only applies to <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> elements in the requested FXG. It will not list any <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> elements from any embedded FXGs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> exists</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>reqId unique request identifier </p> <p>Returns a single property named catalogRecord.exists. The property value is set to "1" if the specified catalog entry exists in the image or default catalog, otherwise it is set to "0". req=exists requests against the /is/content context will indicate the presence or absence of a specified record in the static content catalog. </p> </td> 
  </tr> 
 </tbody> 
</table>

