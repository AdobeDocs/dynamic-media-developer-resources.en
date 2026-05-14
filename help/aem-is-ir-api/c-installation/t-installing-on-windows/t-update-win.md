---
title: Updating from IS 4.7.4 or later
description: Use this procedure when upgrading Dynamic Media Image Serving.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
TQID: 'https://experienceleague.adobe.com/ibeLWHpA-Lk2wiXkSgGL02uMEYH4t8l0xjjXuN9ooiE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# Updating from IS 4.7.4 or later{#updating-from-is-or-later}

Use this procedure when upgrading Dynamic Media Image Serving.

 If you are upgrading from an older version of Image Serving, please contact support for the correct process.

>[!NOTE]
>
>The [!DNL webapps] folder may be deleted on upgrade. Back up the [!DNL webapps] folder before upgrade.

1. Log into your server host with administrative privileges.
1. Extract the contents of the Image Serving distribution zip file.
1. Launch the installation wizard by running `setup/setup.exe`.
1. Select **[!UICONTROL Next]** to advance to the End User License Agreement (EULA), read the license agreement, and select **[!UICONTROL Yes]**.

   The next page displays the previous configuration settings.
1. Click **[!UICONTROL Next]** to start the update installation.

   >[!NOTE]
   >
   >The installer backs up the old server configuration files to the [!DNL BACKUP/] folder.

1. After the installation is complete, select **[!UICONTROL Finish]** to exit the installation wizard.

   Sometimes the installation wizard may ask you to reboot the system.

During an update, the [!DNL ImageServing/conf/server.xml] file is updated to the latest settings. If you have changed or added any values, you should save your existing [!DNL server.xml] and reimplement your changes after the upgrade.

After an update install, consider warming up the HTTP response cache before taking the server live. Refer to the description of the `playlog` utility for details.
