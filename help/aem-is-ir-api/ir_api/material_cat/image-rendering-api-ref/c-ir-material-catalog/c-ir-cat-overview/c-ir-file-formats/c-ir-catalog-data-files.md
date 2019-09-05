---
description: Catalog data files can have any name and file suffix (except .ini).
seo-description: Catalog data files can have any name and file suffix (except .ini).
seo-title: Catalog data files
solution: Experience Manager
title: Catalog data files
topic: Scene7 Image Serving - Image Rendering API
uuid: 3ab4bd1c-2c48-4b12-9418-da5237682f37
index: y
internal: n
snippet: y
---

# Catalog data files{#catalog-data-files}

Catalog data files can have any name and file suffix (except .ini).

Catalog data files can be maintained readily using applications which support tab-delimited text data files, such as Microsoft Excel and Access.

Essentially a two-dimensional table, a catalog data file consists of a header record which identifies the data columns and any number of data records (rows). Fields in both header and data records are separated by single `<TAB>` characters. Records are separated by a single `<CR>` (ASCII code 0xD), a single `<LF>` (ASCII code 0xA), or a `<CR><LF>` pair.

The header record must contain the exact names for each data field. Empty fields are not permitted in the header row. Data field names are not case sensitive. All field names must be unique.

No white space other than the `<TAB>` field separators is permitted in header and data records.

In the data records, two adjacent `<TAB>` characters indicate an empty field. Empty fields will inherit default values from either the catalog attributes or from the server defaults.

Data fields must not contain `<CR>`, `<LF>`, or `<TAB>` characters, unless the data value is of type text and is enclosed by single or double quotation marks. Data fields must not be HTTP-encoded.

Multiple data values in the same field are separated by commas (','), unless otherwise noted.

Columns whose names start with '.' are ignored; this permits storing data in material catalogs which is of no interest to Image Rendering. Columns with unknown header names are ignored and a warning is written to the log file.

Field names may consist of any combination of ASCII letters, numbers, as well as "-" and "_".

One or more columns may be used as index keys. If the same key occurs more than once in the same data file, the later instance will prevail. 
