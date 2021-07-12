---
description: You must set up and configure the IR 3.x compatibility module.
solution: Experience Manager
title: Setup and configure IR 3.x compatibility module
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
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

**Linux Example** 

`cd /usr/local/scene7/ImageServing/webapps/ROOT` 

`cp -r ../ir/* ./` 

`cd WEB-INF` 

Then edit [!DNL web.xml]using your favorite editor to uncomment the `<servlet>` and `<servlet-mapping>` tags. 

**Windows Example** 

Open Explorer and go to `C:\Program Files\Scene7\ImageServing\webapps\ir`. 

Select all files and folders and copy those inside `C:\Program Files\Scene7\ImageServing\webapps\ROOT`. 

Then edit the file `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`,uncommenting the `<servlet>` and `<servlet-mapping>` tags.
