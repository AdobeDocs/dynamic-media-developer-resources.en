---
description: Use these steps to install Image Serving for the first time on Windows.
seo-description: Use these steps to install Image Serving for the first time on Windows.
seo-title: Installing for the first time
solution: Experience Manager
title: Installing for the first time
uuid: 3b28fbc7-6bc9-4619-8f92-c0ae610b8b30
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Business Practitioner"
---

# Installing for the first time{#installing-for-the-first-time}

Use these steps to install Image Serving for the first time on Windows.

1. Log into your server host with administrative privileges.
1. If you have already received a license, copy it to your server, then run the license installation by double-clicking on the file.

   If you do not yet have a license, you may proceed with the installation and install the license later. 
1. Extract the contents of the Image Serving distribution zip file.
1. Run [!DNL setup]/ [!DNL setup.exe] to launch the installation wizard.
1. Click "Next" to advance to the End User License Agreement (EULA), read the license agreement, and click **[!UICONTROL Yes]**.

   The [!DNL Authentication] dialog box displays next. 
1. If a license is already installed, and the license information appears in the [!DNL Authentication] dialog box, click **[!UICONTROL Next]** to continue.

   If you do not have a license, click **[!UICONTROL Request License]**. The next dialog box shows one of your machine's Network Interface Card MAC addresses. Email this MAC address, your company name, and the product you are installing as directed by the prompt.

   **Important:** The license is based on the MAC address of one of the Network Interface Cards installed on this host. If you disable, remove, or replace this card, the license will no longer be recognized as valid. Be sure to obtain a license for the hardware configuration that you will use for IS.

   You may continue to install IS without a valid license and install the license later. To proceed, click **[!UICONTROL Back]** to return to the [!DNL Authentication] dialog box, and then click **[!UICONTROL Next]**. 
1. Proceed to the "Platform Server Admin Settings" page. Enter new values as needed or accept the defaults.

   You can configure the following items:

<table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
 <tbody> 
  <tr> 
   <td> <p> Platform Server HTTP Connection Port </p> </td> 
   <td> <p>Main HTTP listening port for Image Serving and Image Rendering </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Admin Listening Port </p> </td> 
   <td> <p>Admin Listening Port </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Platform Server Cache Size in MB </p> </td> 
   <td> <p>Initial size of the main response cache </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Platform Server Cache Location </p> </td> 
   <td> <p>PS cache folder </p> </td> 
  </tr> 
 </tbody> 
</table>

   Port numbers specified must be unique and not used by other applications or services.

   The next screen provides an opportunity to review the selected settings. 
1. Click **[!UICONTROL Back]** to make changes, or click **[!UICONTROL Next]** to start the installation.
1. Click **[!UICONTROL Finish]** to exit the installation wizard.
