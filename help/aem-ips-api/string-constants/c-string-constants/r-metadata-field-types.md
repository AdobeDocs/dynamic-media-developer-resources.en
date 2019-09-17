---
description: Used by MetadataField/type, saveMetadataFieldParam/fieldType, and createMetadataField/fieldType.
seo-description: Used by MetadataField/type, saveMetadataFieldParam/fieldType, and createMetadataField/fieldType.
seo-title: Metadata Field Types
solution: Experience Manager
title: Metadata Field Types
topic: Scene7 Image Production System API
uuid: 57d292bb-848a-4e6e-bd08-4e6af1f9fc72
---

# Metadata Field Types{#metadata-field-types}

Used by MetadataField/type, saveMetadataFieldParam/fieldType, and createMetadataField/fieldType.

 Syntax 

## Values {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* `Untyped` 
* `Boolean` 
* `BooleanTag`: A special case of `SingleFixedTag` with a non-modifiable dictionary initialized to the values `True` and `False`. 

* `Color` 
* `Date` 
* `Dimension` 
* `FileName` 
* `Float` 
* `Int` 
* `MultiFixedTag`: Zero or more string values from a closed dictionary. Only admin users can modify the dictionary. 
* `MultiTag`: Zero or more string values. 
* `SingleFixedTag`: A single string value from a closed dictionary. If `setAssetMetadata` or `batchSetAssetMetadata` are called with a value not in the dictionary, a fault will be returned. Only admin users can modify the dictionary. 

* `SingleTag`: Any single string value. 
* `String`

