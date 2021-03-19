---
description: Defines search conditions for tag fields.
seo-description: Defines search conditions for tag fields.
seo-title: TagCondition
solution: Experience Manager
title: TagCondition
uuid: c7727267-05b6-4011-9ddf-7f3134e9609b
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Administrator"
---

# TagCondition{#tagcondition}

Defines search conditions for tag fields.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Tag field handle. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> op</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Depends on the tag field type and whether the value or valueArray field is used. 
    <ul id="ul_CC0926425B094B3BB7D70CB392DBDABD">
     <li id="li_09AB923A9A8D4A71917CF59C150E4EF5">If <span class="codeph"> value</span> is passed, <span class="codeph"> op</span> must be the string constant Matches. The condition matches any asset that is associated with the tag value. </li>
     <li id="li_70F18494AB6C454EB611F51F16C19FAD">If <span class="codeph"> valueArray</span> is passed, the op field can be the constant <span class="codeph"> MatchesAny</span> for either single or multivalued tag fields. A <span class="codeph"> MatchesAny</span> condition matches any asset that is associated with at least one of the tag values in <span class="codeph"> valueArray</span>. </li>
     <li id="li_0B25542D7E964B26B15591C45D5C66D0">For multi-valued tag fields, the op field can be set to the constant <span class="codeph"> MatchesAll</span> with the <span class="codeph"> valueArray</span> field. In this case, the condition only matches assets that are associated with all of the tag values in <span class="codeph"> valueArray</span> (possibly in addition to other tag values). </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> value</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> A matching value. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> valueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Multiple matching values. </td> 
  </tr> 
 </tbody> 
</table>

