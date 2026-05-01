---
title: Media set responses
description: The settings in this section apply to the media set responses obtained by the req=set modifier.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
TQID: https://experienceleague.adobe.com/SpqgWIdlOxqS6L3QfIi7vfCgDrK9yP4WpauNJ1GM00M
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Media set responses{#media-set-responses}

The settings in this section apply to the media set responses obtained by the `req=set` modifier.

## PS::fvctx.useCatalogRecordValidation - Caching Policy {#section-9accb087d16548a988993bb30395a6f6}

This property controls the caching policy when determining whether a set response retrieved from a cache must be regenerated. If the property is disabled, the timestamp of the [!DNL catalog.ini] file is used for validation. If property is enabled, the latest `catalog::LastModified` timestamp from all referenced records is used for validation.

## PS::fvctx.nestingLimit - Nesting Limit {#section-280210341f1647fea02590e7069934d2}

The maximum nesting depth of any `req=set` response. If this depth is exceeded, an error is returned.

## PS::fvctx.brochureLimit - Brochure Limit {#section-fe36e47db49244cea7f07e9dd3639440}

The maximum number of e-catalog brochures in the `req=set` response which contains all associated metadata. Once this limit is exceeded, any private maps and user data associated with the brochure item are suppressed.
