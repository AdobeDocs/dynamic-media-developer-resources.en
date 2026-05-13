---
title: Templates
description: Templates may be used to reduce the length and complexity of requests which composite multiple image layers or which include rtf-formatted text.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef49cf8a-4621-4114-aae5-5178f6a5160d
TQID: 'https://experienceleague.adobe.com/FFRoxO7iVDzE7Kta5Vig4RtaPWa890tNHPwsAOcWVCw'
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
# Templates{#templates}

Templates may be used to reduce the length and complexity of requests which composite multiple image layers or which include rtf-formatted text.

Custom variables may be used to further simplify template use. Templates are often set up to allow easy swapping of images or text or setting other options at run-time.

Templates are stored as records in image catalogs, with the template body in the `catalog::Modifier` field, and the `catalog::Path` field empty or specifying a static background image which cannot be changed dynamically.

Templates are specified with the `template=` command or in the path component of the request URL. For most applications it is recommended to use the `template=` command to specify templates. The `template=`command must not occur in the `catalog::PostModifier` field and may only occur in the `catalog::Modifier` field in a nested IS request (that is, in a `src=is{...}` construct). Template records may not be referenced in `src=` or `mask=`commands.

Any `src=` or `mask=`commands embedded in the template may resolve to the main catalog of the request or to a different image catalog. If no `rootId` is specified explicitly, the main catalog is assumed. The template specified with `template=` may also be located in the main catalog or a different image catalog.

It is highly recommended to always include default definitions for all variables used in a template. This way, the image output of the template can always be viewed simply by specifying its `attribute::RootId` and `catalog::Id`, without having to know what variables are used in the template.

The predefined path substitution variable `$object$` can be used to apply the image object specified in the url path to any layer source or mask ( `src=` or `mask=`), even in nested or embedded requests. 

* [Example A](r-example-a.md)
* [Example B](r-example-b.md)
* [Example C](r-example-c.md)
