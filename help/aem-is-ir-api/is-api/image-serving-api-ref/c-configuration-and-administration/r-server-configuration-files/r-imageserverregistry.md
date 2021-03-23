---
description: Contains Image Server configuration settings.
solution: Experience Manager
title: ImageServerRegistry.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
---

# ImageServerRegistry.xml{#imageserverregistry-xml}

Contains Image Server configuration settings.

When modifying this XML file, care must be taken to maintain valid XML syntax, otherwise the Image Server may fail to start.

For changes to take effect, restart the Image Server after editing this file. Only the element values listed below are supported for modification. Edit any other contents of this file only when advised by Dynamic Media technical support.

>[!NOTE]
>
>Do not change the structure of `<imageserverregistry>`, including the order of elements. Use caution when editing this file, otherwise the Image Server may fail to start.

The following illustrates which elements can be changed. Other elements are present which must not be changed. The order of elements below is not reflective of the order in which they must be present in the file.

```
<imageserverregistry>
    <TcpPort> 27345 </TcpPort>    
    <RootPath ./images </RootPath>
    <TempDirectory ./temp </TempDirectory>
    <Log> ./logs/ImageServer.log </Log>
    <TraceClient> 2 </TraceClient>
    <TraceStatsInterval> 600 </TraceStatsInterval>
    <PhysicalMemory> 20 </PhysicalMemory>
    <WorkerThreads> 0 </WorkerThreads>
    <SVGTcpPort> 27346 </SVGTcpPort>
    <MaxRenderRgnPixels> 16 </MaxRenderRgnPixels>
    <MaxSavePixels> 100 </MaxSavePixels>
    <MaxMessageSize> 16 </MaxMessageSize>
    <CacheServerUrl> http://localhost:8080/is/cache/secondary </CacheServerUrl>
    <NumberOfTextServers> 0 </NumberOfTextServers>
    <TextServerTcpPortRange> 27347-27380 </TextServerTcpPortRange>
    <SaveDirectory> ./ </SaveDirectory>
    <RemoteUrlDefaultExpiration> 36000 </RemoteUrlDefaultExpiration>
    <RemoteUrlTimeout> 60 </RemoteUrlTimeout>
    <MaxNonDsfSize> 4 </MaxNonDsfSize>
</imageserverregistry>
```

## Notes {#section-7217f011f69f41e7af4f3983d7776d6f}

Multiple `<RootPath>` elements may be present (one for each source data file folder). Image Server searches the root paths in the order specified to find a particular source file. 
