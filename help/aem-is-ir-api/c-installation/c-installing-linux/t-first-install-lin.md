---
description: This procedure shows how to install Image Serving for the first time on Linux.
seo-description: This procedure shows how to install Image Serving for the first time on Linux.
seo-title: Installing for the first time
solution: Experience Manager
title: Installing for the first time
uuid: 6a9a6dd2-2c69-447a-9628-eba08dc4f6c8
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Business Practitioner"
---

# Installing for the first time{#installing-for-the-first-time}

This procedure shows how to install Image Serving for the first time on Linux.

1. Log in to your server host with root permissions.
1. Create the folder [!DNL /usr/local/scene7/licenses].

   If the Image Serving and/or Image Rendering license key file (with [!DNL .sc8] file suffix) is available, copy it to this folder. Otherwise, proceed with the installation and install the license key later. 
1. Uncompress and untar the Image Serving distribution tar file.
1. Run [!DNL ./install-is], located in the [!DNL Setup] folder, to launch the installation wizard.

   If no license key is found, instructions are displayed describing how to obtain a license file. Do so at this point or proceed with the Image Serving installation and install the license key later. 
1. When the End User License Agreement (EULA) displays, read the license agreement and then enter `y` to proceed.

   The installer displays the prompts listed in the following table.

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Main Listening Port [8080]:</span> </p> </td> 
   <td colname="col2"> <p>Main HTTP listening port for Image Serving and Image Rendering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Admin Listening Port [8083]:</span> </p> </td> 
   <td colname="col2"> <p>Admin listening port. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Maximum HTTP Cache Size (MB) [2000]:</span> </p> </td> 
   <td colname="col2"> <p>Initial size of the main response cache. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Cache Root Folder [/usr/local/scene7/ImageServing/cache]:</span> </p> </td> 
   <td colname="col2"> <p>PS cache folder. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Image Server Owner ID [root]:</span> </p> </td> 
   <td colname="col2"> <p>The user account under which Image Serving servers is to be installed. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Image Server Group ID [root]:</span> </p> </td> 
   <td colname="col2"> <p>The group account under which Image Serving servers is to be installed. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Press **[!UICONTROL Enter]** to accept the default value or specify a different value.

   Make sure all port numbers specified are unique and not used otherwise on this host.

   >[!IMPORTANT]
   >
   >If an account other than root is specified, you must make sure that access permissions for all files and folders the Image Server needs to read and/or write are correctly set up when these folders are reconfigured in the configuration files.
   >
   >Image Serving is now installed to [!DNL /usr/local/Scene7/ImageServing]. Certain Image Rendering contents are installed to [!DNL /usr/local/Scene7/ImageRendering].
   >
   >Towards the end of the installation, the install wizard attempts to start Image Server. If no valid license key is found, the Image Server cannot start. If there is a valid license and Image Server is still not starting up, consult the log files. 

>[!NOTE]
>
>If the license is installed after installing Image Serving, the Image Server must be started manually before use. 
