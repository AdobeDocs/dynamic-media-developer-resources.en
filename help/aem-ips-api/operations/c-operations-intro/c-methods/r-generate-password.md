---
description: Generates a new password.
solution: Experience Manager
title: generatePassword
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 80e7642f-4aec-4ff0-a090-e59b7a065c39
TQID: https://experienceleague.adobe.com/BhTuwhskY-ZE0tGXS8yyG3UvnbN-Y3-0ej16rcx9yWk
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# generatePassword{#generatepassword}

Generates a new password.

 Syntax 

## Authorized User Types {#section-88f7dc11e5c74be281399d8f2e3c9555}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin`
* `TrialSiteAdmin` 
* `TrialSiteUser` 
* `ImagePortalAdmin` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-d516615c906240819a284786efb19863}

**Input (generatePasswordParam)**

None.

**Output (generatePasswordParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  password  | `xsd:string`  | Yes  | A new password.  |

## Examples {#section-f580fefdccec46fe95359e3aef0ed17f}

This code sample generates a password. It is unusual because the request is simply a parameter without any enclosed elements or values. IPS returns a strong password.

**Request** 

```java
<generatePasswordParam xmlns="http://www.scene7.com/IpsApi/xsd">
</generatePasswordParam>
```

**Response** 

```java
<generatePasswordReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <password>1\7aQRn]</password>
</generatePasswordReturn>
```
