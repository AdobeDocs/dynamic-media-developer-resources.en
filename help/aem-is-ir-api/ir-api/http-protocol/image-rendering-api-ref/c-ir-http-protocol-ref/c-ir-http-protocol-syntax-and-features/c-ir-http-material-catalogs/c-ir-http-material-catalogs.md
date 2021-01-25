---
description: Material catalogs offer several features.
seo-description: Material catalogs offer several features.
seo-title: Material catalogs *
solution: Experience Manager
title: Material catalogs *
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 2a2f371e-0982-47c7-b3da-678a5ff6c7a7
---

# Material catalogs *{#material-catalogs}

Material catalogs offer several features.

* Allow persistent definition of materials, including all material properties.

  Materials defined in the material catalog can be referenced using a simple ID, rather than a set of material properties. 
* Provide defaults for certain request attributes, such as the JPEG quality or a default reply image size. 
* Manage vignettes, ICC profiles, and request templates.

Even if no specific material catalogs are defined, all features of material catalogs are available via the default catalog ( [!DNL default.ini]).

While render materials may be specified explicitly in requests using material attributes, in many cases it is more desirable to hide the details of materials from the web site by using material catalogs. src= commands accept catalog references instead of explicit file paths. A catalog entry consists of ` [ *[!DNL catId]*/] *[!DNL itemId]*`, where ` *[!DNL catId]*` identifies a material catalog and ` *[!DNL itemId]*` identifies a record in the catalog. If ` *[!DNL catId]*` is not specified, the session catalog is used (see below).

A catalog record is matched successfully if (a) ` *[!DNL catId]*` matches the `attribute::RootId` value of a material catalog and (b) ` *[!DNL recId]*` matches the catalog::Id value in the same catalog. In case of a successful match, the attributes of the material (including `src=`) are set to the data from the catalog record. If the MSS includes additional attributes for this material besides src=, they override the values from the catalog record.

If ` *[!DNL recId]*` cannot be matched to a catalog entry, then ` *[!DNL catId]*` is replaced with `attribute::RootPath` from the catalog and the resulting path is then assumed to be a simple file path. Other default attributes (e.g. `attribute::Resolution`) may also be inherited from the material catalog.

Vignettes and ICC profiles can be itemized in material catalogs similar to the materials themselves, and given properties. In addition, the vignette map also provides the container for templates.

**See also**

Material Catalog Reference, [ `src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath` 
