---
description: A process that re-rips an existing PDF asset.
solution: Experience Manager
title: RipPdfsJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 7a787b45-3cda-44f2-8357-8b6217b679e0
---
# RipPdfsJob{#rippdfsjob}

A process that re-rips an existing PDF asset.

>[!NOTE]
>
>This job type is deprecated. Transition to `ReprocessAssetsJob` for all future integrations.

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Name </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Handle to the array of PDF files to be ripped. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> createMask</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Determines if you want to create a mask or not. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Manual cropping options. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Automatic cropping options. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:PostTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:PDFOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> illustratorOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>An array of project handles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> emailSetting</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Email settings. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>The URL where the files are being uploaded to. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:ImageServingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Job details for an image serving publish job to be run after the upload is complete. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:ImageRenderingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Job details for an image rendering publish job to be run after the upload is complete. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:VideoPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Job details for a video publish job to be run after the upload is complete. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:InDesignOptions</span> </p> </td> 
   <td colname="col3"> <p>Options for uploading Adobe InDesign files to the image server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:KnockoutBackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>Mask the background for selected images. This lets you overlay them in other layers with a transparency outside of subject image. </p> <p>Optional. </p> <p>See<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Notes {#section-0822e70fa4784131baa5ad0ba8c0fb3b}

Choices for `*CropOptions` include:

* `manualCropOptions` 
* `autoColorCropOptions` 
* `autoTransparentCropOptions`

Choices for `*PublishJob` include:

* `postImageServingPublishJob` 
* `postImageRenderingPublishJob` 
* `postVideoPublishJob`
