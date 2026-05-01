---
title: header
description: HTTP response header element. Optional in <rule> elements.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 40849602-16b2-471b-9128-14653e84a45a
TQID: https://experienceleague.adobe.com/MnetuRzfwotKLJDFo7MkZaLi06hEU0-d1e570qvQwwI
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
# header{#header}

HTTP response header element. Optional in `<rule>` elements.

## Attributes {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name` = "*text*"** : Required. Specifies the name of the HTTP header.

**`Action` = "set" | `"add"`**: Optional. Default is `"set"`, which replaces any current header value. Specify `"add"` so you can append the header value, separated with a comma.

## Data {#section-a387f541396c49d99c29692a38032914}

Header value.

## Description {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

Allows adding new HTTP response headers and adding or replacing values of pre-defined headers. Names and values must conform to HTTP standards. No additional encoding is applied.

Image Serving substitution variables may be used in the header name and the header value. This allows controlling both strings from the request.

## Example {#section-cb5b738b9b93407cb2f4d35af3e59c02}

The following rule applies a custom header when the header value is specified in the request as a variable:

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>

```

This rule is triggered by the following request, setting the HTTP response header `Edge-Control::no-store`:

`http://server/is/image/cat/id?$Edge-Control=no-store`
