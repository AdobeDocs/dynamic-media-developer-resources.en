---
description: You must set up and configure the IR 3.x compatibility module.
seo-description: You must set up and configure the IR 3.x compatibility module.
seo-title: Setup and configure IR 3.x compatibility module
solution: Experience Manager
title: Setup and configure IR 3.x compatibility module
topic: Scene7 Image Serving - Image Rendering API
uuid: 609a6ac9-1a4e-4cca-ab08-aa0f957b0e31
index: y
internal: n
snippet: y
---

# Setup and configure IR 3.x compatibility module{#setup-and-configure-ir-x-compatibility-module}

You must set up and configure the IR 3.x compatibility module.

1. Stop `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. Change to the ImageServer webapps directory.
1. Copy the contents of the [!DNL ir] directory into the [!DNL ROOT] directory.
1. Open [!DNL ROOT/WEB-INF/web.xml] in a text editor.
1. Search for the line `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. Uncomment the `<servlet>` and `<servlet-mapping>` tags.
1. Restart `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
>**Linux Example** 
>
>`cd /usr/local/scene7/ImageServing/webapps/ROOT` 
>
>`cp -r ../ir/* ./` 
>
>`cd WEB-INF` 
>
>Then edit [!DNL web.xml]using your favorite editor to uncomment the `<servlet>` and `<servlet-mapping>` tags. 
>
>**Windows Example** 
>
>Open Explorer and go to [!DNL C:\Program Files\Scene7\ImageServing\webapps\ir]. 
>
>Select all files and folders and copy those inside [!DNL C:\Program Files\Scene7\ImageServing\webapps\ROOT]. 
>
>Then edit the file [!DNL c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml],uncommenting the `<servlet>` and `<servlet-mapping>` tags. 

