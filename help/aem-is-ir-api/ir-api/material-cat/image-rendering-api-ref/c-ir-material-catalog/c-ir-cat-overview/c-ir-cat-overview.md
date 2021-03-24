---
description: Material catalogs provide information about vignettes, materials, and supporting data, such as ICC profiles, to the server.
solution: Experience Manager
title: Material catalog overview *
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# Material catalog overview *{#material-catalog-overview}

Material catalogs provide information about vignettes, materials, and supporting data, such as ICC profiles, to the server.

Each material catalog consists of a required *catalog attribute file* and a set of optional *catalog data files*:

* The vignette map file, which itemizes vignettes and templates and their associated metadata. 
* The material data file, which itemizes materials and specifies the associated texture image files and metadata. 
* The macro definitions file, which provides definitions for request macros. 
* The profile map file, which itemizes ICC color profiles.

Catalog data files are associated with material catalogs by file references in the catalog attribute file. The same catalog data file can be shared by multiple material catalogs.

Catalog attribute files must have a [!DNL .ini] file suffix and must be located in the Image Rendering *catalog folder* ( [!DNL PlatformServer::ir.catalogRootPath]). Catalog data files can be located in the same folder or any other folder accessible to the Render Server.

**Updating material catalogs**

The server continuously monitors the catalog folder and automatically reloads a material catalog, including the associated catalog data files, when it detects that the main catalog attribute file has been changed. Thus, to update material catalogs on the server, first replace all catalog data files that need to be changed, and then replace (or "touch") the catalog attributes file to trigger the catalog reload.

**Default catalog**

The default catalog provides default values for all catalog attributes for all material catalogs. If a particular attribute cannot be found in a specific material catalog, the server will use the corresponding value from the default catalog instead. Similarly, the default catalog can be used to provide defaults for specific catalog data records (materials and ICC profiles). If a particular data record cannot be found in a specific material catalog, the server will attempt to find it in the default catalog instead. This allows material catalogs to be sparsely populated and simplifies management of global attributes and data, such as shared templates, macros, fonts, etc.

In addition, the default catalog provides all attributes and data records (ICC profiles) when no specific material catalog is involved in an operation.

For correct functioning of the Render Server the catalog attributes file for the default catalog must be named [!DNL default.ini], must always exist in the catalog folder, and must be fully populated with all required attributes, excluding `attribute::RootId` and the references to the various catalog data files, which are all optional.

**See also**

`PlatformServer::ir.catalogRootPath` 
