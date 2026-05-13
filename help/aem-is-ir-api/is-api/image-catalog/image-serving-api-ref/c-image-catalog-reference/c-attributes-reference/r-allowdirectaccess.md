---
description: Allow direct access to path-based assets.
solution: Experience Manager
title: AllowDirectAccess
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4000bdf-c21a-4976-82a7-70b2261dee0b
TQID: 'https://experienceleague.adobe.com/h2bcjdutPEZID471oI-MWfxG4trg87bIeyAxvoMyKEA'
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
# AllowDirectAccess{#allowdirectaccess}

Allow direct access to path-based assets.

When this attribute is defined, path-based access is allowed or restricted for the specified object types, depending on whether the `include` or `exclude` keyword is used.

>[!NOTE]
>
>If the `AllowDirectAccess` attribute is not specified, the default value is `exclude`.

* `include` allows access for the specified object types and restricts access for all others. 
* `exclude` restricts access for the specified object types and allows access for all others.

If neither `include` nor `exclude` is specified, `include` is assumed.

The following types can be controlled:

* `SVG` 
* `IS` 
* `STATIC` 
* `FXG` 
* `FLA` 
* `IR_VNT` 
* `IR_MAT`

## Examples {#section-4c3765ebaa4245a799b454fc196f9237}

* Allow direct access only for `IS` and `STATIC` object types

  `AllowDirectAccess=include:IS,STATIC`

* Allow direct access for all object types except `IS` and `STATIC``AllowDirectAccess=exclude:IS,STATIC`

* Allow direct access for *no* object types (that is, include none)

  `AllowDirectAccess=include:`

* Allow direct access for *all* object types (that is, exclude none)

  `AllowDirectAccess=exclude:`

* Equivalent to `include:IS,STATIC` (if `include`/ `exclude` is not present, `include` is assumed)

  `AllowDirectAccess=IS,STATIC`

  Note that is the default value which is used if the `AllowDirectAccess` attribute is not specified for this company. 

* Include none, equivalent to `include:` (if `include`/ `exclude` is not present, `include` is assumed)

  `AllowDirectAccess=`
