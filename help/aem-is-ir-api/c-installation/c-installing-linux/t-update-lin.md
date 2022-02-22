---
title: Updating from IS 4.7.4 or later
description: Use this procedure when upgrading Dynamic Media Image Serving on Linux®.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54733fcc-c4e3-4501-8a3d-000778678bdb
---
# Updating from IS 4.7.4 or later{#updating-from-is-or-later}

Use this procedure when upgrading Dynamic Media Image Serving on Linux®.

If you are upgrading from an older version of Image Serving, please contact support for the correct process.

The [!DNL webapps] folder can be deleted on upgrade. Please back up the [!DNL webapps] folder before upgrade.

1. Log in to your server host with root privileges.
1. Uncompress and untar the Image Serving distribution tar file.
1. In the [!DNL setup] folder, run [!DNL `./install-is`] to launch the installation wizard.

   The update installer checks the integrity and version of the installed package. If successful, the End User License Agreement ("EULA") is displayed.
1. Read the license agreement and then enter **[!UICONTROL y]** to proceed with the installation.

   The installer backs up the old server configuration files to the [!DNL BACKUP/] folder.

   When the installation is complete, the following message is shown:

   `Image Server was started successfully`

During an update, the [!DNL ImageServing/conf/server.xml] file is updated to the latest settings. If you have changed or added any values, save your existing [!DNL server.xml] and reimplement your changes after the upgrade.

After an update install, consider warming up the HTTP response cache before taking the server live. Refer to the description of the [!DNL playlog] utility for details.
