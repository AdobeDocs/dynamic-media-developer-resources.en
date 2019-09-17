---
description: The viewer displays search result regions over the main view to highlight words or phrases found in the catalog.
seo-description: The viewer displays search result regions over the main view to highlight words or phrases found in the catalog.
seo-title: Search effect
solution: Experience Manager
title: Search effect
topic: Dynamic media
uuid: 3a076ff8-2da5-4020-8a77-8f5a256afefe
---

# Search effect{#search-effect}

The viewer displays search result regions over the main view to highlight words or phrases found in the catalog.

<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>

**CSS properties of the main viewer area**

The appearance of search result regions is controlled with the following CSS class selector:

`.s7ecatalogsearchviewer .s7searcheffect .s7region`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS property </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background </span> </p> </td> 
   <td colname="col2"> <p>Background of search result region. </p> </td> 
  </tr> 
 </tbody> 
</table>

Example - to set up search result regions with a semi-transparent, yellow fill:

```
.s7ecatalogsearchviewer .s7searcheffect .s7region { 
 background: rgba(255,255,0, 0.5); 
}
```

