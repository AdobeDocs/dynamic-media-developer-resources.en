---
description: The RLA class represents an RLA (Run-Length Encoded, Version A) file that has been loaded into memory.
seo-description: The RLA class represents an RLA (Run-Length Encoded, Version A) file that has been loaded into memory.
seo-title: class s7vampy.rla.RLA(rla)
title: class s7vampy.rla.RLA(rla)
uuid: 2d8fd35c-1982-4fc9-a873-bd29be517c9f
index: y
internal: n
snippet: y
---

# class s7vampy.rla.RLA(rla){#class-s-vampy-rla-rla-rla}

The RLA class represents an RLA (Run-Length Encoded, Version A) file that has been loaded into memory.

RLA instances are immutable.

RLA class instances can only be created using [ `s7vampy.open_rla()`](../../../c-s7vampy-api-reference/c-functions/r-s7vampy.open-rla.md#reference-e0869994e3fc4a22befc9a8dc2dfe1dc).

`name [str, read-only]`

Name of the RLA instance.

`size [tuple, read-only]`

Size in pixels (width, height). 
