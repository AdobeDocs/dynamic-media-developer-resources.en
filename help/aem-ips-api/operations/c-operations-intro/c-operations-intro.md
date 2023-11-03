---
description: Describes the common operation parameters handled by the IPS Web Service API.
solution: Experience Manager
title: Operations methods
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 020c8e63-ad4e-4c0d-8da6-b51efb2b89a5
---
# Operations methods{#operations-methods}

This section describes the common operation parameters handled by the IPS Web Service API.

For a complete description of each operation parameter, see [Operation parameters](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md).

## Handles: About {#section-094ce1afa6244fa5b2c762f44ffdca1c}

Handles reference IPS objects returned by certain API operations. You can also pass handles as parameters to subsequent operation calls. Handles are string data types ( `xsd:string`).

Handles are intended for use during a single application session only. Furthermore, you should make handles persistent because their format can change between IPS releases. When you write interactive applications, you implement session timeouts and discard all handles between sessions, particularly after an IPS upgrade. When you write non-interactive applications, call the appropriate operations to retrieve handles each time the application is run. The following Java/Axis2 code samples show incorrect and correct code execution:

**Incorrect Handle Code**

This code sample is incorrect because it contains a hard-coded value (555) for the company handle. 

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**Correct Handle Code**

This code sample is correct because it calls `getCompanyInfo` to return valid handle. It does not rely on a hard-coded value. Use this method-or other IPS API equivalent-to return the required handle. 

```
GetCompanyInfoParam companyInfoParam = new GetCompanyInfoParam(); 
companyInfoParam.setCompanyName("My Company"); GetCompanyInfoReturn companyInfoReturn = ipsApi.getCompanyInfo(companyInfoParam, authHeader); 
String companyHandle = companyInfoReturn.getCompanyInfo().getCompanyHandle(); 
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle(companyHandle); //CORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

## Common Handle Types {#section-e683ac8283284f9688e63f51a494f7a0}

**companyHandle**

Most operations require you to set a company context by passing in a `companyHandle` parameter. The company handle is a pointer returned by certain operations such as `getCompanyInfo`, `addCompany`, and `getCompanyMembership`.

**userHandle**

The `userHandle` parameter is an optional parameter for operations that target a specific user. By default, these operations target the calling user (the user whose credentials are passed in for authentication). However, admin users with the proper permissions can specify a different user. For example, the `setPassword` operation normally sets the password of the authenticated user, but an admin can use the `userHandle` parameter to set the password for a different user.

For operations that require a company context (using the `companyHandle` parameter), both the authenticated and target users must be members of the specified company. For operations that do not require a company context, the authenticated and target users must both be members of at least one common company.

The following operations can retrieve user handles:

* `getUsers` 
* `getAllUsers` 
* `getUserInfo` 
* `getCompanyMembers` 
* `getGroupMembers` 
* `addUser`

**accessUserHandle and accessGroupHandle**

By default, operations that require access permissions (read, write, delete) operate in the permission context of the calling user. Certain operations allow you to modify this context with the `accessUserHandle` or `accessGroupHandle` parameter. The `accessUserHandle` parameter allows an admin to impersonate another user. The `accessGroupHandle` parameter allows the caller to operate in the context of a specific user group.

**responseFieldArray and excludeFieldArray**

Some operations allow the caller to restrict which fields are included in the response. Limiting fields can help reduce the time and memory required to process the request and reduce the size of the response data. The caller can request a specific list of fields by passing a `responseFieldArray` parameter, or with an enumerated a list of excluded fields by way of the `excludeFieldArray` parameter.

Both `responseFieldArray` and `excludeFieldArray` specify fields by using a node path separated by `/`. For example, to specify that `searchAssets` returns only the name, last modified date, and metadata for each asset refer to the following: 

```
<responseFieldArray> 
   <items>assetArray/items/name</items> 
   <items>assetArray/items/lastModified</items> 
   <items>assetArray/items/metadataArray</items> 
</responseFieldArray>
```

Similarly, to return all fields (except for permissions): 

```
<excludeFieldArray> 
   <items>assetArray/items/permissions</items> 
</excludeFieldArray>
```

Note that the node paths are relative to the return node root. If you specify a complex type field without any of its sub-elements (for example, `assetArray/items/imageInfo`), then all of its sub-elements are included. If you specify one or more sub-elements in a complex type field (for example, `assetArray/items/imageInfo/originalPath`), then only those sub-elements are included.

If you do not include `responseFieldArray` or `excludeFieldArray` in a request, all fields are returned.

**Locale**

Since IPS 4.0, the IPS API supports setting the locale context of an operation by passing the `authHeader` locale parameter. If the locale parameter is not present, the HTTP header `Accept-Language` is used. If this header is also not present, the default locale for the IPS server is used.

Certain operations also take explicit locale parameters, which may be different from the operation locale context. For example, the `submitJob` operation takes a `locale` parameter that sets the locale used for job logging and email notification.

Locale parameters use the format `<language_code>[-<country_code>]`

Where the language code is a lower-case, two-letter code specified by ISO-639 and the optional country code is an upper-case, two-letter code specified by ISO-3266. For example, the locale string for US English is `en-US`.
