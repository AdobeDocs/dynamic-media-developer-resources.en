---
title: Set up and configure IR 3.x compatibility module
description: Set up and configure the IR 3.x compatibility module.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
TQID: 'https://experienceleague.adobe.com/ce7CdClFrrIFb7fhZRKQ7XBpsNm4BTgwVFHPXy3BXhw'
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
# Set up and configure IR 3.x compatibility module{#setup-and-configure-ir-x-compatibility-module}

1. Stop `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. Change to the ImageServer webapps directory.
1. Copy the contents of the [!DNL ir] directory into the [!DNL `ROOT`] directory.
1. Open [!DNL `ROOT/WEB-INF/web.xml`] in a text editor.
1. Search for the line `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. Uncomment the `<servlet>` and `<servlet-mapping>` tags.
1. Restart `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Linux® example** 

`cd /usr/local/scene7/ImageServing/webapps/ROOT` 

`cp -r ../ir/* ./` 

`cd WEB-INF` 

Then edit [!DNL `web.xml`] using your favorite editor to uncomment the `<servlet>` and `<servlet-mapping>` tags. 

**Windows example** 

Open Explorer and go to `C:\Program Files\Scene7\ImageServing\webapps\ir`. 

Select all files and folders and copy those inside `C:\Program Files\Scene7\ImageServing\webapps\ROOT`. 

Then edit the file `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`, uncommenting the `<servlet>` and `<servlet-mapping>` tags.

