---
description: Parameter common to all viewers.
seo-description: Parameter common to all viewers.
seo-title: config
solution: Experience Manager
title: config
topic: Dynamic media
uuid: 9e9bb580-a33a-4405-b05c-56962d702145
index: y
internal: n
snippet: y
---

# config{#config}

Parameter common to all viewers.

 ` config= *`configId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configId </span> </span> </p> </td> 
   <td colname="col2"> <p>Catalog/ID for the viewer configuration. </p> <p> Specifies an image catalog entry that contains the viewer configuration properties in <span class="codeph"> catalog::UserData </span>. When this command is present, the viewer sends a <span class="codeph"> req=userdata </span> command for <span class="codeph"> configId </span> to the server and extracts properties from the reply. The properties are used to initialize the viewer. If the URL string specifies the same properties, they override the values from <span class="codeph"> catalog::UserData </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

All viewer commands that can be specified in `catalog::UserData` expect `asset`, `serverUrl`, `contentUrl`, `searchServerUrl`, and `config` itself.

## Properties {#section-10ee45d637134e0fbcd943c62578cb78}

Optional.

## Default {#section-d411e450028c460392cb8508f8ccc5d9}

None.

## Example 1 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

An image catalog named 2020 contains the entry `preset-oct`. The `catalog::UserData` field of this catalog entry includes the following data:

```
style=customStyle.css
```

Load the viewer with the following command:

```
config=2020/preset-oct
```

This is equivalent to the following commands specified explicitly in the URL:

```
style=customStyle.css
```

## Example 2 {#section-577fce5ddbee43fc96d88b2055df47aa}

An image catalog named 2019 contains the entry `spin-oct`. The `catalog::UserData` field of this catalog entry includes the following data:

```
zoomStep=3 
maxZoom=200
```

Load the viewer with the following command:

```
config=2019/spin-oct
```

This is equivalent to the following commands specified explicitly in the URL:

```
zoomStep=3&maxZoom=200
```

## Example 3 {#section-2b3a42c3926e4eb19fa14434def9195f}

A viewer preset named `Shoppable_Banner` includes the following data:

```
style=etc/dam/presets/css/html5_interactiveimage.css
```

Load the viewer with the following command:

```
config=/etc/dam/presets/viewer/Shoppable_Banner
```

This is equivalent to the following commands specified explicitly in the URL:

`style=etc/dam/presets/css/html5_interactiveimage.css`

## Example 4 {#section-98dd1cc6b2a24375a1bd572fa83be35c}

A viewer preset named `Shoppable_Video_Dark` contains the following data:

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

Load the viewer with the following command:

```
config=/etc/dam/presets/viewer/Shoppable_Video_Dark
```

This is equivalent to the following commands specified explicitly in the URL:

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

## Example 5 {#section-19b988551d1d492a9079948e0b04b38f}

A viewer preset named `Carousel_Dotted_light` the following data:

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```

Load the viewer with the following command:

```
config=/etc/dam/presets/viewer/Carousel_Dotted_light
```

This is equivalent to the following commands specified explicitly in the URL:

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```

