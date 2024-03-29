---
title: Media set responses
description: The settings in this section apply to the media set responses obtained by the req=set modifier.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
---
# Media set responses{#media-set-responses}

The settings in this section apply to the media set responses obtained by the `req=set` modifier.

## PS::fvctx.useCatalogRecordValidation - Caching Policy {#section-9accb087d16548a988993bb30395a6f6}

This property controls the caching policy when determining whether a set response retrieved from a cache must be regenerated. If the property is disabled, the timestamp of the [!DNL catalog.ini] file is used for validation. If property is enabled, the latest `catalog::LastModified` timestamp from all referenced records is used for validation.

## PS::fvctx.nestingLimit - Nesting Limit {#section-280210341f1647fea02590e7069934d2}

The maximum nesting depth of any `req=set` response. If this depth is exceeded, an error is returned.

## PS::fvctx.brochureLimit - Brochure Limit {#section-fe36e47db49244cea7f07e9dd3639440}

The maximum number of e-catalog brochures in the `req=set` response which contains all associated metadata. Once this limit is exceeded, any private maps and user data associated with the brochure item are suppressed.
