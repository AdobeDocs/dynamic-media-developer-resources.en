---
description: Use this procedure when upgrading Dynamic Media Image Serving.
solution: Experience Manager
title: Updating from IS 4.7.4 or later
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
---
# Updating from IS 4.7.4 or later{#updating-from-is-or-later}

Use this procedure when upgrading Dynamic Media Image Serving.

 If you are upgrading from an older version of Image Serving, please contact support for the correct process.

>[!NOTE]
>
>The [!DNL webapps] folder may be deleted on upgrade. Back up the [!DNL webapps] folder before upgrade.

1. Log into your server host with administrative privileges.
1. Extract the contents of the Image Serving distribution zip file.
1. Run setup/setup.exe to launch the installation wizard.
1. Click **[!UICONTROL Next]** to advance to the End User License Agreement (EULA), read the license agreement, and click **[!UICONTROL Yes]**.

   The next page displays the previous configuration settings. 
1. Click **[!UICONTROL Next]** to start the update installation.

   >[!NOTE]
   >
   >The installer backs up the old server configuration files to the [!DNL BACKUP/] folder.

1. Once the installation is complete, click "Finish" to exit the installation wizard.

   In some cases the installation wizard may ask to reboot the system. 

During an update, the [!DNL ImageServing/conf/server.xml] file is updated to the latest settings. If you have changed or added any values you should save your existing [!DNL server.xml] and reimplement your changes after the upgrade. 

After an update install, consider warming up the HTTP response cache prior to taking the server live. Refer to the description of the `playlog` utility for details.
