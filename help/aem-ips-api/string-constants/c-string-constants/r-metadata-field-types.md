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

* [!DNL `Untyped`] 
* [!DNL `Boolean`] 
* [!DNL `BooleanTag`]: A special case of [!DNL `SingleFixedTag`] with a non-modifiable dictionary initialized to the values [!DNL `True`] and [!DNL `False`]. 

* [!DNL `Color`] 
* [!DNL `Date`] 
* [!DNL `Dimension`] 
* [!DNL `FileName`] 
* [!DNL `Float`] 
* [!DNL `Int`] 
* [!DNL `MultiFixedTag`]: Zero or more string values from a closed dictionary. Only admin users can modify the dictionary. 
* [!DNL `MultiTag`]: Zero or more string values. 
* [!DNL `SingleFixedTag`]: A single string value from a closed dictionary. If `setAssetMetadata` or `batchSetAssetMetadata` are called with a value not in the dictionary, a fault will be returned. Only admin users can modify the dictionary. 

* [!DNL `SingleTag`]: Any single string value. 
* [!DNL `String`]

