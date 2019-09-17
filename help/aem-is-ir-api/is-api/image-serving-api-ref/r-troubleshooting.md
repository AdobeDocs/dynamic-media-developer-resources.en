---
description: This section contains solutions to problems that have occasionally occurred with Image Serving.
seo-description: This section contains solutions to problems that have occasionally occurred with Image Serving.
seo-title: Troubleshooting
solution: Experience Manager
title: Troubleshooting
topic: Scene7 Image Serving - Image Rendering API
uuid: 39fdaf86-004b-4553-bde0-0367f3ef76b8
---

# Troubleshooting{#troubleshooting}

This section contains solutions to problems that have occasionally occurred with Image Serving.

 **General**

ImageServer now keeps an install log and a backup folder of all files changed during an upgrade install. This file and folder may be found at the root of the Image Serving installation directory.

**When starting the Image Server, the startup script stalls with the message "start pending" (LINUX only)**

This may indicate a problem with the Image Serving License, such as a missing license file or an expired temporary license. A valid license file must be located in [!DNL /usr/local/scene7/licenses].

**Image Server stalls or crashes and the Image Server log file indicates not enough space or "resource temporarily unavailable in file [!DNL IgcVirtualMemory.cpp]"**

The reason for this error message is that Image Server has failed to allocate the amount of memory it was configured to use.

* Check the Physical Memory setting in [!DNL ImageServerRegistry.xml]. It should be no more than 50%, less if other memory-intensive applications are running on the same system. The default is 20%. 
* Make sure that swap space on the Server is at least double the size of physical RAM. Low swap space settings can cause this problem.

**Actual disk space used by the cache folder exceeds ` *[!DNL cache.maxSize]*`set in [!DNL PlatformServer.conf]**

This does not indicate a problem. The file system overhead is not included in the Platform Server's disk cache setting. The total amount reported by the system may be substantially more than the setting. It is recommended to reserve twice as much disk space as is specified in ` *[!DNL cache.maxSize]*`.

**Broken images in the is-docs examples**

This occurs if Image Server is not running. It also occurs if the catalog root path or image root path has been changed from the installation default, but the example images and catalogs have not been moved to the new locations. Check the Image Server Root Path value in configuration files. If necessary, move the demo folder that contains the example images to the current image root, and move [!DNL sample*.*] to the current catalog root.

The examples also assume that certain settings in [!DNL default.ini] are standard (e.g. obfuscation or locking must not be enabled).

**Too many cache misses after substantial uptime**

Depending on server usage, performance may be improved by increasing Platform Server disk cache size if disk space is available. Settings can be changed by manually editing configuration files. See documentation.

**Log files are taking up too much disk space**

The Image Server and Platform Server start a new log file every day. By default these are placed in [!DNL *[!DNL install_root]*/ImageServing/logs]. Log file size, number of logs kept and log content can be configured. See documentation.

**If you have anti-virus software installed on your server**

It is recommended that you turn off scanning for Image Serving directories. Otherwise, scanning high volume read/write directories (such as cache, images, fonts, profiles and catalog directories) will cause problems.

**Digimarc causes performance problems for zoom images**

Do not use Digimarc on images that will be zoomed. The performance will not be acceptable. If necessary, create a separate catalog for images to be used for zooming and disable Digimarc for this catalog. 
