---
description: null
seo-description: null
seo-title: Questions About Performance
solution: Experience Manager
title: Questions About Performance
topic: Scene7 Image Authoring
uuid: d52adb33-7dfd-460b-9ae7-ef34ec445a2e
index: y
internal: n
snippet: y
---

# Questions About Performance{#questions-about-performance}

## How can I improve performance? {#how-can-i-improve-performance}

There are several performance-related settings in [!DNL Image Authoring]:

* The [!DNL Show preview thumbnail in image File Open dialogs] setting on the [!DNL General] tab of the [!DNL Preferences] dialog box (available from the [!DNL Edit] menu) can be unchecked to improve performance when opening images or vignettes whose version is 55 or higher. 

* The [!DNL Browse IPS Folders] option on the [!DNL IPS] tab of the [!DNL Preferences] dialog box (available from the [!DNL Edit] menu) can be unchecked to speed up the display of the [!DNL IPS Export] dialog box, if you have a lot of IPS folders. However, if you uncheck this option, you must specify the complete path to a folder when you upload images to IPS. 

* The [!DNL Redraw the preview texture during vertex moves] setting on the [!DNL Flowline Page] tab of the [!DNL Preferences] dialog box (available from the [!DNL Edit] menu) can be unchecked to improve performance on the [!DNL Flowline] page. 

* Lower the [!DNL Static] and [!DNL Moving] values in the [!DNL Advanced/Meshing] option on the [!DNL Flowline Page] tab of the [!DNL Preferences] dialog box. This lowers the resolution of the texture being moved. 

* On the [!DNL Flowline] page, select the [!DNL Mesh] tool and set the [!DNL Display] to [!DNL Flowlines]. When you move flowlines and vertexes, you won't see the mesh but performance does improve. 

* The [!DNL Use OpenGL for all graphics] and [!DNL Display image in full resolution] settings on the [!DNL 3D Modeling Page] tab of the [!DNL Preferences] dialog box (available from the [!DNL Edit] menu) can be unchecked to improve performance on the [!DNL 3D Modeling] page. 

* If the vignette has many overlapping objects, going to the [!DNL Render] page can be very slow as it tries to render all overlapping objects. To turn this off, uncheck [!DNL Show overlap objects when renderer is reset] on the [!DNL Render Page] tab of [!DNL Preferences]. 

* If [!DNL Image Authoring] launches slowly, make sure that the [!DNL Preferences] on the [!DNL IPS] tab are pointing to an active IPS server and your computer can connect to IPS. [!DNL Image Authoring] checks the connection on launch now. 

* If there are many items in [!DNL Material History], [!DNL Favorite Materials], [!DNL Preview Materials], or [!DNL Material Templates], then this slows down the launching of [!DNL Image Authoring].

