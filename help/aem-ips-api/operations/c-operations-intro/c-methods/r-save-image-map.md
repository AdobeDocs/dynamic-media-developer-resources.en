---
description: Create a new image map or edit an existing map.
solution: Experience Manager
title: saveImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 91e40549-9b26-41f2-a3ab-7e9bec8f9ba7
---
# saveImageMap{#saveimagemap}

Create a new image map or edit an existing map.

 Syntax 

## Authorized User Types {#section-9ef194a67b3546fb82ed7bb294bc2714}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

>[!NOTE]
>
>The user must have read and write access to the asset.

## Parameters {#section-64f7f5fd8f954fba9fa30eeee556863a}

**Input (saveImageMapParam)** 

<table id="table_49649036F46941D2B1F28515674E533B"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> The handle to the company with the image map you want to save. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> The handle to the image asset to which the image map belongs. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageMapHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> The handle to the image map. Creates an image map if NULL. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> The name of the image map that is created or saved. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> shapeType </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> Choice of Region Shape. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> region </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> A comma-delimited list of points that define the region. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> action </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> <p>The <span class="codeph"> href </span> value associated with the image map as specified in the IPS interface. </p> <p>To obtain the <span class="codeph"> href </span> value, click the image in the IPS interface, copy and paste the URL into this element, and then format the IPS URL as a proper URL. For example, <span class="codeph"> &amp; </span> becomes <span class="codeph"> &amp;amp; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> position </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int </span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> The order in the list of image maps (the Z axis). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> enabled </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean </span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"></td> 
  </tr> 
 </tbody> 
</table>

**Output (saveImageMapReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`imageMapHandle`*`  | `xsd:string`  | Yes  | The handle to the new or edited image map.  |

## Examples {#section-fdac488b640f427c8aa3d549c5032851}

This code sample creates a new image map for an asset. It uses a shape type determined by a region shape string constant and returns a handle to the new image map.

**Request** 

```
<saveImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <companyHandle>47</companyHandle> 
   <assetHandle>24266|1|17062</assetHandle> 
   <name>My Image Map</name> 
   <shapeType>Rectangle</shapeType> 
   <region>0,10,0,10</region> 
   <action>http://s7oslo.macromedia.com/scene7/browse/MoreInfo.jsp?assetID=24266&amp; 
   iRow=1&iRows=1&amp;strSearchType=image</action> 
   <position>0</position> 
</saveImageMapParam>
```

**Response** 

```
<saveImageMapReturn xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <imageMapHandle>34191|8|554</imageMapHandle> 
</saveImageMapReturn>
```
