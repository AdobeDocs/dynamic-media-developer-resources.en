---
description: Upload setting to process ZIP and TAR files as primary assets (None) or to extract and upload their contents (UnCompress).
seo-description: Upload setting to process ZIP and TAR files as primary assets (None) or to extract and upload their contents (UnCompress).
seo-title: UnCompressOptions
solution: Experience Manager
title: UnCompressOptions
uuid: 1e6827db-8c5e-47db-b7ff-4e681e107e57
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Administrator"
---

# UnCompressOptions{#uncompressoptions}

Upload setting to process ZIP and TAR files as primary assets (None) or to extract and upload their contents (UnCompress).

>[!NOTE]
>
>`None` is default.

## Parameters {#section-10e49e27f60743da970a4ff1c4587eab}

<table id="table_89C2F7CDB24848459E47F1F7F58D91BA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> process</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Controls ZIP and TAR archive file processing. Provides 2 options: 
     <ul id="ul_F34E2F3B9B74450CA7E76BD9FD7137C2">
      <li id="li_E982468ED814446593B0C0A3F3D729FB"><span class="codeph"> None:</span> Process as primary assets. </li>
      <li id="li_4A45DA99592B4EF7A1FE0A946A835104"><span class="codeph"> UnCompress:</span> Extract and process contents. </li>
     </ul><p>Note: String constants are case sensitive. Use <span class="codeph"> UnCompress</span>, not <span class="codeph"> uncompress</span> or <span class="codeph"> unCompress</span>. </p></p> </td> 
  </tr> 
 </tbody> 
</table>

## Example {#section-48fd14af768a436284c31692038579a8}

```
 <!-- uncompress zip/tar/gzip files -->
            <element name="unCompressOptions" type="types:UnCompressOptions" minOccurs="0"/>
    <complexType name="UnCompressOptions">
        <sequence>
            <!-- Options: None (default),UnCompress -->
            <element name="process" type="xsd:string"/>
        </sequence>
    </complexType>
```

## Used By {#section-b2a829cf5511412e968bb2000f85cc31}

The `unCompressionOptions` type is used by:

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6) 
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) 
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

