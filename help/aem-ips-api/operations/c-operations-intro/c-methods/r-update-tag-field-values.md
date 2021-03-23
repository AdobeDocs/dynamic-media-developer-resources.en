---
description: Updates tag dictionary values for a tag field.


solution: Experience Manager
title: updateTagFieldValues

feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
---

# updateTagFieldValues{#updatetagfieldvalues}

Updates tag dictionary values for a tag field.

 Syntax 

## Authorized User Types {#section-0372b742b1344979b0668faacb36fcc6}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-0a3a4bab026746238c9d4009caf42e94}

**Input (updateTagFieldValuesParam)** 

<table id="table_15F354FBC043464080BC975AE35E03A4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Required </th> 
   <th colname="col4" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> Company handle. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> Tag field handle. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:TagValueUpdateArray</span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4">Array of tag field values that you want to update. <p>Note:  Updates tag string values only. Does not affect asset associations. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (updateTagFieldValuesReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`successCount`*`  | `xsd:int`  | Yes  | The number of successfully updated tag fields.  |
|  `*`warningCount`*`  | `xsd:int`  | Yes  | The number of warnings generated when the operation attempted to update tag fields.  |
|  `*`errorCount`*`  | `xsd:int`  | Yes  | The number of errors generated when the operation attempted to update tag fields.  |
|  `*`warningDetailArray`*`  | `types:TagValueUpdateFaultArray`  | No  | The array of details associated with the assets that generated warnings when the operation attempted to update tag fields.  |
|  `*`errorDetailArray`*`  | `types:TagValueUpdateFaultArray`  | No  | The array of details associated with the assets that generated errors when the operation attempted to update tag fields.  |

## Examples {#section-bb4dcf97044c4675974c9b8d27674001}

**Request** 

```java
<updateTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <updateArray>
      <items>
         <oldValue>Nurth</oldValue>
         <newValue>North</newValue>
      </items>
      <items>
         <oldValue>Suth</oldValue>
         <newValue>South</newValue>
      </items>
      <items>
         <oldValue>East</oldValue>
         <newValue>West</newValue>
      </items>
      <items>
         <oldValue>Banana</oldValue>
         <newValue>Pear</newValue>
      </items>
   </updateArray>
</updateTagFieldValuesParam>
```

**Response** 

```java
<updateTagFieldValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>2</errorCount>
   <errorDetailArray>
      <items>
         <value>East</value>
         <code>30001</code>
         <reason>New tag value 'West' already exists.</reason>
      </items>
      <items>
         <value>Banana</value>
         <code>30001</code>
         <reason>Tag value 'Banana' not found.</reason>
      </items>
   </errorDetailArray>
</updateTagFieldValuesReturn>
```

