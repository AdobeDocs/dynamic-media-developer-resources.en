---
description: Used by MetadataField/type, saveMetadataFieldParam/fieldType, and createMetadataField/fieldType.
solution: Experience Manager
title: Metadata Field Types
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: cbbe55f2-bd22-44f5-9440-f58fb45b8d9a
TQID: https://experienceleague.adobe.com/LC8aixlfWyJWulsMsQaI7-iiO-dKx9TC0pimZ5fj51I
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
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
* [!DNL `SingleFixedTag`]: A single string value from a closed dictionary. If `setAssetMetadata` or `batchSetAssetMetadata` are called with a value not in the dictionary, a fault is returned. Only admin users can modify the dictionary. 

* [!DNL `SingleTag`]: Any single string value. 
* [!DNL `String`]
