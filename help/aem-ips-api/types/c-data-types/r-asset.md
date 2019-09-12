---
description: An object or container in the folder hierarchy.
seo-description: An object or container in the folder hierarchy.
seo-title: Asset
solution: Experience Manager
title: Asset
topic: Scene7 Image Production System API
uuid: 758ac593-98d8-4366-a723-a06435c7fd3c
index: y
internal: n
snippet: y
---

# Asset{#asset}

An object or container in the folder hierarchy.

 Syntax 

## Parameters {#section-0f2abb29deaf4d73bbbd0a5a2dc9ca3b}

<table id="table_C58EF9963CB34179A9D6C9F0F6FF24F2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> acoInfo</span> </span> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> animatedGifInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:AnimatedGifInfo</span> </td> 
   <td colname="col3"> Details about an animated GIF file. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Asset handle. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSetInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> cabinetInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:CabinetInfo</span> </td> 
   <td colname="col3"> Properties for a cabinet asset type. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> created</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Date and time the asset was uploaded. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createUser</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Email address of the user who created the asset. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> cssInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:CssInfo</span> </td> 
   <td colname="col3"> Details about a CSS file. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> cuePointInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excelInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fileName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Returns the virtual filename. The full virtual file path is <span class="codeph"> folder</span>+<span class="codeph"> fileName</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> flashInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Folder that contains an asset. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Handle to the asset's parent folder. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fontInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:fontInfo</span> </td> 
   <td colname="col3"> Properties for a font asset. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> iccProfileInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:IccProfileInfo</span> </td> 
   <td colname="col3"> Properties for an ICC profile asset. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> illustratorInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ImageInfo</span> </td> 
   <td colname="col3"> Properties for an image asset. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ipsImageUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Relative URL representing a thumbnail view of the asset. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> javascriptInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:JavascriptInfo</span> </td> 
   <td colname="col3"> Details about a JavaScript file. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastModified</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Date and time the asset was last modified. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastModifyUser</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Email address of the user who last modified the asset. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> layerViewInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:LayerViewInfo</span> </td> 
   <td colname="col3"> Properties for a layer view asset. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> maskInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> masterVideoInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:MetadataArray</span> </td> 
   <td colname="col3"> Array of metadata values associated with the asset. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Asset name. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfSettingsInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:PdfSettingsInfo</span> </td> 
   <td colname="col3"> Properties of a PDF settings asset. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> permissions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> powerPointInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> premiereExpressInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projects</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> List of project names. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> psdInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Sets a flag to indicate if an asset should be published or not. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> renderSceneInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:RenderSceneInfo</span> </td> 
   <td colname="col3"> Properties of a render scene asset. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> rtfInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> subType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Generic asset subtype that supports subtype values (for example, <span class="codeph"> AssetSet</span>). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> svgInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:SvgInfo</span> </td> 
   <td colname="col3"> Properties of an SVG asset. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> swcInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:SwcInfo</span> </td> 
   <td colname="col3"> Properties of an SWC asset. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> templateInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:TemplateInfo</span> </td> 
   <td colname="col3"> Properties of a template asset. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Indicates if an asset is in the trash or live (see "Trash State" for values). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Asset type. See <a href="../../string-constants/c-string-constants/r-asset-types.md#reference-2fe75d230663419d88632d30f1144a10" format="dita" scope="local"> Asset Types</a> for values. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoCaptionInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:VideoCaptionInfo</span> </td> 
   <td colname="col3"> <p>Properties of a video caption asset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> <p>Properties of a video asset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> viewerPresetInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ViewerPresetInfo</span> </td> 
   <td colname="col3"> Properties of a viewer preset asset. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> viewerSwfInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ViewerSwfInfo</span> </td> 
   <td colname="col3"> Properties of a viewer SWf asset. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> vignetteInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:VignetteInfo</span> </td> 
   <td colname="col3"> Properties of a vignette asset. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> watermarkInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:WatermarkInfo</span> </td> 
   <td colname="col3"> Properties of a watermark asset. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> windowCoveringInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:WindowCoveringInfo</span> </td> 
   <td colname="col3"> Properties of a window covering asset. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> wordInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xmlInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:XmlInfo</span> </td> 
   <td colname="col3"> Properties of an XML asset. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xslInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:XslInfo</span> </td> 
   <td colname="col3"> Properties of an XSL asset. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> zipInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Code Phrase </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

