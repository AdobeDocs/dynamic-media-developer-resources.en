---
description: In addition to the space necessary to install the software, Image Serving has the following disk space requirements 
solution: Experience Manager
title: Disk space requirements and recommendations
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Business Practitioner"
---

# Disk space requirements and recommendations{#disk-space-requirements-and-recommendations}

In addition to the space necessary to install the software, Image Serving has the following disk space requirements:

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Description/ Default Location/ Set With</b> </th> 
   <th class="entry"> <b>Calculation/ Recommendation</b> </th> 
   <th class="entry"> <b>Comments</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>Source images, fonts, ICC profiles</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/images </span> <span class="codeph"></span> </p> <p> <span class="codeph"> IS::RootPaths </span> </p> </td> 
   <td> <p>Varies; see comments below. </p> </td> 
   <td> <p>Only needs to be accessible to the Image Server; the servers never modify data. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>HTTP response data cache</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/is-response </span> </p> <p> <span class="codeph"> PS::ResponseCacheFolders </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer::cache.maxSize </span> x 2; at least 2 GB recommended. </p> </td> 
   <td> <p>This cache also stores nested/embedded data and foreign source images. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Image catalog data cache</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/catalog </span> </p> <p> <span class="codeph"> CS::CatalogCacheFolder </span> </p> </td> 
   <td> <p>Allow the catalog folder to use 1.5x the space. </p> </td> 
   <td> <p>Populated when catalogs are loaded initially. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Log data</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/logs </span> </p> <p> <span class="codeph"> PS::LogFolder </span> </p> <p> <span class="codeph"> IS::LogFile </span> </p> <p> <span class="codeph"> SV::LogFile </span> </p> </td> 
   <td> <p>100 Mbytes or more. </p> </td> 
   <td> <p>Varies depending on logging configuration and server use. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Image Server temporary files</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/temp </span> </p> <p> <span class="codeph"> IS::TempDirectory </span> </p> <p> <span class="codeph"> SV::TempDirectory </span> </p> </td> 
   <td> <p>100 MBytes is sufficient for most uses. </p> </td> 
   <td> <p>Short-lived data; may be needed for source images other than PTIFFs and certain response image formats. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Disk space requirements for source images {#section-317da75099ad480d9a461c7e706d4f1c}

It is recommended to convert all source images to the pyramid TIFF file format (PTIFF) using the Image Converter command-line tool (IC). This conversion ensures optimal runtime performance of Image Serving for all applications. While the Image Server can process all source file formats accepted by IC, Dynamic Media does not provide support for such uses.

When you use PTIFF files, the following rules of thumb can help you determine the space requirements.

*`total_space`* (bytes) = *`number_of_images`* x(2000 + *`avg_pixel_count`* x *`avg_num_components`* x *`p_factor`*)

* *`avg_pixel_count`* The average pixel size (width x height) of all original source images. For example, if the original images are typically around 2k x 2k pixels, this would be 4M pixels. 
* *`avg_num_components`* Depends on the type of images. For mostly RGB images it is 3, for mostly CMYK or RGBA images it is 4. Use 3.5 if half the images are RGB and the other half is RGBA. 
* *`p_factor`* Depends on the compression type and quality set when the images are converted with IC.

<table id="table_89995BECF30243569954819D07DA2A2F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>PTIFF compression</b> </th> 
   <th class="entry"> <b><i>p_factor</i></b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>Uncompressed </p> </td> 
   <td> <p> 33 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Deflate-Compression </p> </td> 
   <td> <p> 25-0.75, depending on the image </p> </td> 
  </tr> 
  <tr> 
   <td> <p>JPEG Compression </p> </td> 
   <td> <p> 1 (typical for JPEG quality 95) </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>This approximation does not account for file system overhead. The actual space on disk may be substantially larger.

**Example**

An Image Serving deployment expects to use 30,000 low-resolution legacy images, with an average size of 500x500 RGB pixels. New print-quality image data is expected to be added at a rate of 10,000 per year. The typical CMYK image size will be 4k x 6k bytes. All data will be JPEG compressed at high quality. The total amount of disk space after 3 years of use is estimated as follows:

*`total_space`* = 30,000 x (2k + 0.5k x 0.5k x 3 x 0.1) + 3 x 10,000 x (2k + 4k x 6k x 4 x 0.1) = 2.2 G + 268 GB = approximately 270 GB

For guaranteed best quality, deflate (zip) compression could be employed. Assuming a *`p_factor`* of 0.4, the total amount of disk space required is approximately 4 times larger. In this case, slightly more than 1 TB. 
