---
description: Gets assets associated with a specified asset and details about their relationship.
seo-description: Gets assets associated with a specified asset and details about their relationship.
seo-title: getAssociatedAssets
solution: Experience Manager
title: getAssociatedAssets
uuid: 70c2f8aa-9104-42b0-b85b-14f90f1ead52
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
---

# getAssociatedAssets{#getassociatedassets}

Gets assets associated with a specified asset and details about their relationship.

 Syntax 

## Authorized User Types {#section-453cc706400345778713cda249bfac16}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `TrialSiteUser` 
* `ImagePortalAdmin` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-d11d0dab59e94e89b466123a0ebfa82e}

**Input (getAssociatedAssetsParam)** 

<table id="table_DBB97A6507EB48479FFFD2184FF8F07C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Name </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Required </p> </th> 
   <th colname="col4" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Yes </p> </td> 
   <td colname="col4"> <p>Handle to the company that owns the asset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Yes </p> </td> 
   <td colname="col4"> <p>Asset handle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:StringArray</span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>The array of response fields desired. See response- FieldArray/excludeFieldArray in the Introduction. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:StringArray</span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>The array of excluded response fields. See response- FieldArray/excludeFieldArray in the Introduction. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (getAssociatedAssetsReturn)** 

<table id="table_B894B4B6EFA24359A0250A8A4523EA8D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Name </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Required </p> </th> 
   <th colname="col4" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> containerArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:AssetArray</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Array of set and template assets containing the speci- fied asset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> memberArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:AssetArray</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Array of assets contained by the specified set or template asset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> layerReferenceArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:AssetArray</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Array of assets referenced in a layer or template URL. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ownerArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:AssetArray</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Array of assets that own the specified asset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> derivedArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:AssetArray</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Array of assets that were used to generate the specified asset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generatorArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:GenerationInfoArray</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>The <span class="codeph"> generatorArray</span> lists the way this asset was created. For example, if <span class="codeph"> assetHandler</span> was an image page of a PDF, then this would contain the PDF processor tool and reference the PdfFile asset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generatedArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:GenerationInfoArray</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>The <span class="codeph"> generatedArray</span> inverts the way this asset was created. For example, the <span class="codeph"> generatedArray</span> could contain the list of images generated from this <span class="codeph"> assetHandler</span> if this was a PdfFile asset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAsset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:Asset</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>The thumb asset information associated with the request asset. If no thumb asset is assigned, the field is omitted in the response. </p> </td> 
  </tr> 
 </tbody> 
</table>

You can use the parameters `responseFieldArray` or `excludeFieldArray` to limit the response size. In particular, the `GenerationInfo` items returned in `generatorArray` or `generatedArray` default to include both the originator and the generated asset records. For a PDF asset type, this behavior results in unwanted multiple copies of the "originator" PDF asset record in the response. You can eliminate this issue by adding `generatedArray/items/originator` to `excludeFieldArray`. Or, you can specify an explicit list of response fields that you want to include in `responseFieldArray`.

## Examples {#section-8946ea4b9cb94912a8408249c897f192}

The following basic example is a request for the handle of the generator for an image that is extracted from a PDF. It includes a `containerArray` of length one with an item including the `assetHandle` of the PDF.

**Request** 

```java
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:beta="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
   <soap:Body>
      <beta:getAssociatedAssetsParam>
         <beta:companyHandle>c|11</beta:companyHandle>
         <beta:assetHandle>a|197</beta:assetHandle>
         <beta:responseFieldArray>
            <beta:items>containerArray/items/assetHandle</beta:items>
         </beta:responseFieldArray>
      </beta:getAssociatedAssetsParam>
   </soap:Body>
</soap:Envelope>
```

**Response** 

```java
<soapenv:Envelope xmlns:soapenv="http://www.w3.org/2003/05/soap-envelope">
   <soapenv:Body>
      <getAssociatedAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
         <containerArray>
            <items>
               <assetHandle>a|207</assetHandle>
            </items>
         </containerArray>
      </getAssociatedAssetsReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

The inverse of the example above is the following:

**Request** 

```java
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:beta="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
   <soap:Body>
      <beta:getAssociatedAssetsParam>
         <beta:companyHandle>c|11</beta:companyHandle>
         <beta:assetHandle>a|177</beta:assetHandle>
        <beta:responseFieldArray>
           <beta:items>generatedArray/items/originator/assetHandle</beta:items>
         </beta:responseFieldArray>
      </beta:getAssociatedAssetsParam>
   </soap:Body>
</soap:Envelope>
```

**Response** 

```java
<soapenv:Envelope xmlns:soapenv="http://www.w3.org/2003/05/soap-envelope">
   <soapenv:Body>
      <getAssociatedAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
         <generatedArray>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
         </generatedArray>
      </getAssociatedAssetsReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

In this next example, a group is added to a company with `groupHandleArray`. This example uses one group only.

**Request** 

```java
<ns1:addGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray><ns1:items>225</ns1:items></ns1:groupHandleArray>
</ns1:addGroupMembershipParam>
```

**Response**

None. 
