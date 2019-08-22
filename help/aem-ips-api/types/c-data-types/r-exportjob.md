---
description: Job type to allow authorized export of previously uploaded files.
seo-description: Job type to allow authorized export of previously uploaded files.
seo-title: ExportJob
solution: Experience Manager
title: ExportJob
topic: Scene7 Image Production System API
uuid: 22832120-6fc2-4e36-b072-cd1fd4a14c3b
index: y
internal: n
snippet: y
---

# ExportJob{#exportjob}

Job type to allow authorized export of previously uploaded files.

ExportJob does not support the following asset types:

* Image Sets 
* Render Sets 
* Spin Sets 
* Media Sets 
* Multi-bitrate Sets 
* Video Sets 
* eCatalogs 
* Offer Sets

<table id="table_D8F3FD30D15648BFA5B980D3DC0A5AB1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> types:HandleArray</span> </p> </td> 
   <td colname="col3" valign="top"> <p>List of <span class="codeph"> assetHandle</span> which are required to be exported. See <a href="../../types/c-data-types/r-handle-array.md#reference-1b93fefb5477459faf9253b54349b5f9" type="reference" format="dita" scope="local"> HandleArray</a>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fmt</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>Specifies the type of <span class="codeph"> export.Possible Values</span>: [orig, convert] </p> <p> 
     <ul id="ul_16EF4B14100C4C7AA464CA9CF7F11D1C"> 
      <li id="li_DAB2844CC55145C88A18A1F8EC4527F9">If <span class="codeph"> fmt=orig</span>, the assets are exported as original </li> 
      <li id="li_07F2F8D159934D889FDC1022AB12B564">If <span class="codeph"> fmt=convert</span>, the assets are converted to the format specified in the <span class="codeph"> is_modifer</span> or <span class="codeph"> macro</span> input parameters </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> is_modifier</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>Specifies the <span class="codeph"> ImageServer</span> rendering URL string, which is appended to the ExportJob <span class="codeph"> convert</span> request. </p> <p>Refer to the <a href="http://microsite.omniture.com/t2/help/en_US/s7/is_ir_api/" scope="external" format="html"> IS documentation</a> for details about sending the IS modifiers. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> macro</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p></p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>Choice of email setting. Possible values: </p> <p> 
     <ul id="ul_0EEDAE11B7CD4C53A6E4B2B8CB2CF730"> 
      <li id="li_F235F93828594ED78C6D464440F953FF"> <span class="codeph"> All</span> </li> 
      <li id="li_59E14E7EBFA64432A5FAC15DA21A0521"> <span class="codeph"> Error</span> </li> 
      <li id="li_BFE0B52CADD14CC1BA1AF42AB0AA1CE1"> <span class="codeph"> ErrorAndWarning</span> </li> 
      <li id="li_BE3AA67E14FB487B8B9CD6EF3D58824C"> <span class="codeph"> JobCompletion</span> </li> 
      <li id="li_409C68AD0D244975BFB86B08609E0146"> <span class="codeph"> None</span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> clientId</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>Specifies the IP address of the client or customer who initiated the export request. </p> <p> <p>Note:  this parameter is not actively populated currently and is strictly reserved for future usage only. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

For ExportJob requests where `fmt=convert` and both `is_modifier` and `macro` are provided, the destination file respects the format provided by `macro`. For example:

```
input_file = fileToExport.jpg
is_modifer = &fmt=png
macro=$test$ 
output_file = fileToExport.tiff
```

