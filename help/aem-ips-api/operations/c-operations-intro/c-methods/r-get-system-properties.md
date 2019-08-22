---
description: Retrieves all system properties in a single request.
seo-description: Retrieves all system properties in a single request.
seo-title: getSystemProperties
solution: Experience Manager
title: getSystemProperties
topic: Scene7 Image Production System API
uuid: a669f265-2a9c-4851-a03c-3a6c0e45430d
index: y
internal: n
snippet: y
---

# getSystemProperties{#getsystemproperties}

Retrieves all system properties in a single request.

 Syntax 

## Authorized User Types {#section-fc311ce90a54400fa95b9dd36b756e23}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser` 
* `ImagePortalUser` 
* `TrialSiteAdmin` 
* `TrialSiteUser`

## Parameters {#section-b2a4fb7068424223aec87c50f0586d73}

**Input (getSystemPropertiesParam)**

None.

**Output (getSystemPropertiesReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`propertyArray`*`  | `types:PropertyArray`  | Yes  | An array of system properties.  |

## Examples {#section-728cc16fe9954b2daa035b4d4d4b4ce6}

This code sample returns an array of system properties. Response truncated for brevity.

**Request** 

```java
<getSystemPropertiesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10"/>
```

**Response** 

```java
<getSystemPropertiesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10"> 
   <propertyArray> 
      <items> 
         <name>SvgRenderEnabled</name> 
         <value>true</value> 
      </items> 
      <items> 
         <name>SwfRootUrl</name> 
         <value>/SWFs/</value> 
      </items> 
      ... 
   </propertyArray> 
</getSystemPropertiesReturn>
```

