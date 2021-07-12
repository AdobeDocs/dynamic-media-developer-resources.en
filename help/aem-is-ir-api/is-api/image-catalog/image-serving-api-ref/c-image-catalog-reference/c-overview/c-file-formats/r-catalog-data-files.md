---
description: Catalog data files can have any name and file suffix (except .ini). They can be maintained readily using applications which support tab-delimited text data files, such as Microsoft Excel and Access.
solution: Experience Manager
title: Catalog data files
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4aa20abe-4f84-470b-b5a1-3d9246ab1792
---
# Catalog data files{#catalog-data-files}

Catalog data files can have any name and file suffix (except .ini). They can be maintained readily using applications which support tab-delimited text data files, such as Microsoft Excel and Access.

Essentially a two-dimensional table, a catalog data file consists of a header record that identifies the data columns and any number of data records (rows). Fields in both header and data records are separated by single `<TAB>` characters. Records are separated by a single `<CR>` (ASCII code `0xD`), a single `<LF>` (ASCII code `0xA`), or a `<CR><LF>` pair.

The header record must contain the exact names for each data field. Empty fields are not permitted in the header row. Data field names are not case sensitive. All field names must be unique.

Space characters cannot be used as field separators. No spaces are permitted in the header record. In data records, any spaces at the beginning or end of a data field are considered part of that data field.

In the data records, two adjacent `<TAB>` characters indicate an empty field. Empty fields may inherit default values from either the catalog attributes or from the server defaults.

Data fields can optionally be enclosed by double quotation marks. They must not contain `<CR>`, `<LF>`, or `<TAB>` characters, unless the data value is of type text and is enclosed by double quotation marks. Data fields must not be HTTP-encoded.

Multiple data values in the same field are separated by commas, unless otherwise noted.

Columns whose names start with "." are ignored. This permits storing data in image catalogs, which is of no interest to Image Serving. Columns with unknown header names are ignored and a warning is written to the log file.

Field names may consist of any combination of ASCII letters, numbers, as well as "-" and "_".

One or more columns may be used as index keys. If the same key occurs more than once in the same data file, the later instance prevails.
