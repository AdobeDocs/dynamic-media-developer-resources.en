---
description: Used by MetadataField/type, saveMetadataFieldParam/fieldType, and createMetadataField/fieldType.


solution: Experience Manager
title: Metadata Field Types

feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Administrator
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

