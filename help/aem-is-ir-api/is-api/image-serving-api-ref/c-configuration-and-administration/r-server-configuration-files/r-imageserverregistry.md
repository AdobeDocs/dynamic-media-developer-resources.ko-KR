---
description: 이미지 서버 구성 설정을 포함합니다.
seo-description: 이미지 서버 구성 설정을 포함합니다.
seo-title: ImageServerRegistry.xml
solution: Experience Manager
title: ImageServerRegistry.xml
topic: Scene7 Image Serving - Image Rendering API
uuid: cc401f75-1eb1-40fe-8308-eaaf9e14f906
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---


# ImageServerRegistry.xml{#imageserverregistry-xml}

이미지 서버 구성 설정을 포함합니다.

이 XML 파일을 수정할 때 유효한 XML 구문을 유지하기 위해 주의해야 합니다. 그렇지 않으면 이미지 서버를 시작할 수 없습니다.

변경 사항을 적용하려면 이 파일을 편집한 후 이미지 서버를 다시 시작합니다. 아래 나열된 요소 값만 수정에 대해 지원됩니다. Scene7 기술 지원 센터에서 권장하는 경우에만 이 파일의 다른 내용을 편집합니다.

>[!NOTE]
>
>요소의 순서를 포함하여 `<imageserverregistry>`의 구조를 변경하지 마십시오. 이 파일을 편집할 때 주의하십시오. 그렇지 않으면 이미지 서버를 시작하지 못할 수 있습니다.

다음은 변경할 수 있는 요소를 보여 줍니다. 변경할 수 없는 다른 요소가 있습니다. 아래의 요소 순서는 파일에 있어야 하는 순서대로 반영되지 않습니다.

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

## 주의 {#section-7217f011f69f41e7af4f3983d7776d6f}

여러 `<RootPath>` 요소가 있을 수 있습니다(각 소스 데이터 파일 폴더에 대해 하나). 이미지 서버는 특정 소스 파일을 찾기 위해 지정된 순서대로 루트 경로를 검색합니다.
