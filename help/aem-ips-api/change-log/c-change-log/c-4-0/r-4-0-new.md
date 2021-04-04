---
description: Describes new and implemented changes for the IPS API v4.0.
solution: Experience Manager
title: New Additions and Changes

feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: f07562a8-71e9-4d98-9d0c-5bb32a7e0ef1
---
# New Additions and Changes{#new-additions-and-changes}

Describes new and implemented changes for the IPS API v4.0.

Implemented side-by-side API versions with separate WSDLs and schema namespaces.

* Previous API versions: `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`. 
* SPS 4.0 version: `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

Added `PostScriptOptions/alpha` field.

Added `VideoRootUrl` and `SwfRootUrl` properties for `getProperty` operation.

Added optional `appName` and `appVersion` params to `authHeader` to track calling application. Added logging to `ipsApiService.log`.

Added an optional `serviceUrl` param to the WSDL generation servlet. This is particularly useful for debug proxies. For example: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

Implemented `getZipEntries` operation.

Implemented search ranges and typed comparison values for system field conditions.

Added `'Asset'` asset type string constant, primarily to allow cross-asset metadata fields.

Implemented `trashState` param for `searchAssets`.

Implemented `getAssetPublishHistory` operation.

Added optional `faultHttpStatusCode` SOAP header to enable fault handling in Flex. For Flex, use `<faultHttpStatusCode>200</faultHttpStatusCode>`. The default status code for fault responses is `500 (Internal Server Error)`.

Added operations to restore assets from the trash and empty assets from the trash.

Implemented CRUD operations.

Added enabled flag to `ImageMap` type and `saveImageMap` operation.

Added support for Optimize Remaining Files jobs.

Added `setAssetsPublishState` for bulk publish state updates.

Added `ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings`.

Deprecated `saveMetadataField` operation in favor of new `createMetadataField` and `updateMetadataField` operations.

Implemented `deleteAssetsParam` batch delete operation.

Implemented `moveAssetsParam` batch move operation.

Implemented `deleteMetadataField` operation.

Implemented `get/setImageRenderingPublishSettings`, `get/set/create/updateVignettePublishFormat` operations.

Implemented `getAssetCounts`.

Added support to `setImageSetMembers` for including `RenderSet` members in `ImageSet` assets.

Added `replaceImage` operation.

Added `copyImage` operation.

Added `setUrlModifier` operation and `urlModifier/urlPostApplyModifier` fields for `LayerViewInfo`, `TemplateInfo`, and `WatermarkInfo`.

Added `createDerivedAsset` operation. Currently the `ownerHandle` must reference an Image asset and the type may be `AdjustedView` or `LayerView`.

Added `createTemplate` operation. Currently this can be called to create Template or Watermark assets.

IPS company settings, `CompanySettings`, ported to Web services API.

Added `excludeByproducts` filter flag to `searchAssets` operation. Setting this flag to true runs `PSDlayer` images and PDF ripped images.

Added `getGenerationInfo` operation.

Added `SystemMessage` property name to `getProperty` operation.

Modified some asset type string constants to match the corresponding Asset Info fields.

* WordDoc: Word 
* ExcelDoc: Excel 
* PowerPointDoc: PowerPoint 
* RTFDoc: Rtf

Modified result format of batch operations to summarize success, warnings, and errors.

Implemented `batchSetAssetMetadata` batch metadata operation.

Implemented support for app-specific data.

Implemented support for boolean flags for `createTemplate`, `extendLayers`, and `extractText` for upload jobs to control process of Photoshop processing (similar to changes for add file uploads).

Implemented `setImageMaps` and `setZoomTargets` operations.

Implemented `ViewerPreset` operations. The recognized types are:

* `VideoPlayer` (Video only publishes these viewers.) 
* `Brochure` 
* `BasicZoom` 
* `AdvancedZoom` 
* `Spin` 
* `Custom types`

Viewer skins support two parameters: `skinFg` and `skinBg`. Backend code will do all the processing required to maintain backward compatibility.

Implemented `getAssociatedAssets` operation.

Added `ReprocessAssets` job type to allow reprocessing of previously uploaded primary source files, including reripping PDFs and reoptimizing images.

Renamed `PropertySetType` field type to `propertyType`. This affects the `createPropertySetType` parameter and `getPropertySetType/getPropertySetTypes` response.

Implemented `batchSetImageFields` operation to support setting image user data and other editable image fields.

47 Added fileSize field to various asset info types:

* `VignetteInfo` 
* `CabinetInfo` 
* `WindowCoveringInfo` 
* `IccProfileInfo` 
* `FontInfo` 
* `XslInfo` 
* `ViewerSwfInfo` 
* `XmlInfo` 
* `SvgInfo` 
* `ZipInfo` 
* `VideoInfo` 
* `AcoInfo` 
* `PdfInfo` 
* `PsdInfo` 
* `FlashInfo` 
* `InDesignInfo` 
* `PostScriptInfo` 
* `IllustratorInfo` 
* `WordInfo` 
* `ExcelInfo` 
* `PowerPointInfo` 
* `IllustratorInfo` 
* `WordInfo` 
* `ExcelInfo` 
* `PowerPointInfo` 
* `RTFInfo`

Implemented `getActivePublishContexts` operation. This operation returns an array of publish context names with active publish servers for the specified company. Current publish context names are:

* `ImageServing` 
* `ImageRendering` 
* `Video`

Implemented `getSearchStrings` operation. It returns an array of search strings for the given asset.

Added locale parameters for jobs and a mechanism to set the locale for API operations. The locale string should be formatted as `<language_code>[-<country_code>]`. The language code is a lowercase, two-letter code as specified by ISO-639, and the optional country code is an uppercase, two-letter code as specified by ISO-3166.

Added optional locale parameter to the `authHeader` SOAP header to set the locale for API operations. If this parameter is not present, the HTTP header `Accept-Language` will be used. If this header is also not present, the default locale for the IPS server will be used.

Added get/set support for strongly typed metadata fields.

Implemented SOAP and HTTP header support for gzip response control.

Added `gzipResponse` flag to `authHeader`. If it is not present, the API will also check the HTTP `Accept-Encoding` header.

Added support to searchAssets for strongly typed metadata field conditions.

* For all field types, value may be passed with a string comparison operator ( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`) 
* For Boolean fields, `boolVal` may be passed with the `Equals` op. 
* For Int fields, `longVal` may be passed with a numeric comparison operator ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) or `minLong/maxLong` may be passed with a numeric range operations ( `Between, NotBetween`). 
* For Float fields, `doubleVal` may be passed with a numeric comparison operator ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) or `minDouble/maxDouble` may be passed with a numeric range operations ( `Between, NotBetween`). 
* For Date fields, you can pass `dateVal` with a numeric comparison operator ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) or you can pass minDate/maxDate with a numeric range operations ( `Between, NotBetween`).

Added description, `jobSubType`, and `originalJobName` fields to `JobLog` type.

* `originalJobName` is the job name submitted to `submitJob` (without any uniqueness suffixes or follow-on job names). 
* `jobSubType` is currently only used by `ImageServingPublishJob` jobs (where it is one of `full`, `increment, fullwithsearch,` or `fulloverride`). 
* `description` is currently an empty string for all job types, but will eventually contain summary job information, such as the upload path.

In addition, the following fields are not included with both `getJobLogs` and `getJobLogDetails`. In prior versions they were only available with `getJobLogDetails`.

* `endDate` (if the job has completed). 
* `fileDuplicateCount` (previously it was always `0` with `getJobLogs`) 
* `fileUpdateCount` (previously was always `0` with `getJobLogs` and included in `fileSuccessCount`; it is now split out into separate fields).

Added assetHandle field to `JobLogDetail` type.

Added optional description parameter to `submitJob`. This is passed through for retrieval in `getScheduledJobs`, `getActiveJobs`, and `getJobLogs`.

Deprecated the SKU system field. The field is ignored if it is passed in as a `SystemFieldCondition` to `searchAssets`.

Added `excludeAssetTypeArray` filter to `searchAssets`.

Added `MaskInfo` type to `Asset`.

Added new Asset Types for management by IPS:

<table id="table_DCCE936B797A448598C30E3B344525A5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Asset type </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Illustrator </span> </p> </td> 
   <td colname="col2"> <p>Adobe Illustrator file. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PostScript </span> </p> </td> 
   <td colname="col2"> <p>EPS and PostScript files. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> WordDoc </span> </p> </td> 
   <td colname="col2"> <p>Microsoft Word document for files ending with .doc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc </span> </p> </td> 
   <td colname="col2"> <p>Microsoft Excel document for files ending with .xls. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc </span> </p> </td> 
   <td colname="col2"> <p>Microsoft PowerPoint document for files ending with .ppt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc </span> </p> </td> 
   <td colname="col2"> <p>RTF file for files uploaded ending with .rtf. </p> </td> 
  </tr> 
 </tbody> 
</table>

Added additional options to `UploadDirectoryJob` and `UploadUrlsJob` to control processing of Postscript, Illustrator, and PDF files independently. All existing jobs will provide the necessary parameters to the each of the 3 processing pipelines so that they will function exactly as done today. The original `PostScriptOptions` block is used to set the processing for Illustrator and EPS/PS files. Optionally, specific file options blocks can be supplied to specify processing. The list of changes includes:

<table id="table_D4E5ACCB2D144D05A5FA0129AA5F9344"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Field </p> </th> 
   <th colname="col2" class="entry"> <p>Parameter </p> </th> 
   <th colname="col3" class="entry"> <p>Value </p> </th> 
   <th colname="col4" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" morerows="1"> <p> <span class="codeph"> PostScriptOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> process </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> None </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> Rasterize </span>(default) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>Only manage the asset and do not create any derivatives upon upload. </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>Render the EPS and PostScript file into an image at the prescribed resolution and color space. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>Optional. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Takes effect when rasterizing the file into an image. It will create a transparent back- ground if the original file is defined in this way for overlaying logos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> IllustratorOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> process </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> None </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> Rasterize </span> (default) </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>Only manage the asset and do not create any derivatives upon upload. </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>Render the file into an image at the prescribed resolution and color space. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolution </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>Rasterizing resolution. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> colorspace </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Target color space for rendering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>Optional. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Takes affect when rasterizing the file into an image. Creates a transparent background if the original file is defined in this way for creating overlaying logos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> process </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> None </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> Rasterize </span> (default) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>Only manage the asset and do not create any derivatives upon upload. </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>Render the file into an image at the prescribed resolution and color space. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolution </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>Rasterizing resolution. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> colorspace </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Target color space for rendering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Defines whether to combine a multiple page PDF into an eCatalog after rendering (default is true). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Defines whether words from the PDF are extracted into the DB for later supplying to a search server (default is false). </p> </td> 
  </tr> 
 </tbody> 
</table>

You can also query from `getScheduledJobs`.

Modified the `webservice.gzip.response` configuration property to take one of the following values:

<table id="table_FCBBF1643DC84F5CBF81DCA6B552E0C4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Value </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> never </span> </p> </td> 
   <td colname="col2"> <p>Do not gzip response. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> soap </span> </p> </td> 
   <td colname="col2"> <p>Gzip response only if authHeader/gzipResponse is true. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> accept </span> </p> </td> 
   <td colname="col2"> <p>Gzip if authHeader/gzipResponse is true, or no gzipResponse header is present and HTTP Accept-Encoding header includes gzip. (Default). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always </span> </p> </td> 
   <td colname="col2"> <p>Always gzip response, regardless of header values. Use this value only for debugging purposes. </p> </td> 
  </tr> 
 </tbody> 
</table>
