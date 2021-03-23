---
description: Group files into sets using an asset handle list array.


solution: Experience Manager
title: AutomatedSetGenerationJob

feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
---

# AutomatedSetGenerationJob{#automatedsetgenerationjob}

Group files into sets using an asset handle list array.

 Syntax 

## Parameters {#section-939b2e6946a64238be3709fec2cd0b84}

<table id="table_0E031B2014B646BDA2A94D7E0B55DD5B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:HandleArray</span> </td> 
   <td colname="col3">An array of asset handles used to create the set. <p>By default, 1000 is the maximum number of assets you can have in the array. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> destFolder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Path to the folder where you want to save the sets. Saves to company root folder by default. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Sets a flag to indicate if the assets should be published or not. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:AutoSetCreationOptions</span> </td> 
   <td colname="col3">An array of set generation scripts you can run on the uploaded files. See <a href="../../types/c-data-types/r-auto-set-creation-options.md#reference-58b42b39e53345aeb87cd1adc864e7ff" format="dita" scope="local"> AutoSetCreationOptions</a></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Set up an automated email notification for the job. </p> </td> 
  </tr> 
 </tbody> 
</table>

**emailSetting Options**

The `emailSetting` parameter includes the following options: 

|  Option  | Returns  |
|---|---|
| `All` | All job notifications (errors, warnings, completion) to the specified recipient.  |
| `Error` | Job errors to the specified recipient.  |
| `ErrorAndWarning` | Job errors and warnings to the specified recipient.  |
| `JobCompletion` | A job completion notification to the specified recipient.  |
| `None` | The job does not send any job notifications to the specified recipient.  |

## Example {#section-d01ee7671f274a1fa12737e8df91d2cf}

```
<complexType name="AutomatedSetGenerationJob">
  <sequence>
    <element name="assetHandleArray" type="types:HandleArray"/>
    <element name="destFolder" type="xsd:string" minOccurs="0"/>
    <element name="readyForPublish" type="xsd:boolean"/>
    <element name="autoSetCreationOptions" type="types:AutoSetCreationOptions"/>
    <element name="emailSetting" type="xsd:string"/>
  </sequence>
</complexType>
```

