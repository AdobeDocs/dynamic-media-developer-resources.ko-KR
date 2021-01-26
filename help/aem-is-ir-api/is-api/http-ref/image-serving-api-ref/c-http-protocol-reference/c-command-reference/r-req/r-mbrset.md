---
description: 다중 비트 전송률 데이터.
seo-description: 다중 비트 전송률 데이터.
seo-title: mbrSet
solution: Experience Manager
title: mbrSet
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 829c44ce-c66a-49a9-ba69-9e8e94ef8921
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---


# mbrSet{#mbrset}

다중 비트 전송률 데이터.

`req=mbrSet[,text|xml[, *`encodingfmtType `*]][&fmt= *``*]`

<table id="simpletable_D2B8704E09B34337870A257CD7CB5C56"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 인코딩</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> fmtType</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> f4m | m3u8</span> </p></td> 
 </tr> 
</table>

net path id와 연결된 비디오 세트의 유효한 비디오 항목에 해당하는 URL 목록 및 해당 비트 전송률 목록이 포함된 텍스트 또는 xml 응답을 반환합니다.

이제 유효한 비디오 항목에 `catalog::VideoBitRate`에 대한 값이 들어 있다는 이전의 요구 사항이 완화되었습니다. `catalog::VideoBitRate`*또는* `catalog::AudioBitRate`*또는* `catalog::TotalStreamBitRate`에 대한 값을 포함할 수 있습니다. 비디오 항목이 유효하려면 이러한 항목 중 하나만 정의해야 합니다. `catalog::Path` 및 유효한 비디오 파일 확장명에 대한 요구 사항은 변경되지 않았습니다.

응답은 Apple 및 Flash 스트리밍 서버에서 소비하기 위한 것으로 이러한 사양에 구조적으로 일치합니다. URL은 접두어 `attribute::HttpAppleStreamingContext` 및 `attribute::HttpFlashStreamingContext`을 사용하여 생성됩니다.

m3u8 응답에는 비디오 세트에 있는 경우 mp4 파일만 포함됩니다. mp4 파일이 없으면 이러한 응답에는 f4v 파일만 포함됩니다. mp4 파일이나 f4v 파일이 없으면 응답이 비어 있습니다.

f4m 응답은 비디오 세트에 있는 경우 f4v 파일만 포함합니다. f4v 파일이 없으면 이러한 응답에는 mp4 파일만 포함됩니다. f4v 파일이나 mp4 파일이 없으면 응답이 비어 있습니다.

f4m/m3u8 응답에 나타나는 비트 전송률은 `catalog::TotalStreamBitRate`(적절한 단위로 변환된)의 값에 해당합니다. `catalog::TotalStreamBitRate`이(가) 정의되지 않은 경우 `catalog::VideoBitRate` 및 `catalog::AudioBitRate`의 합계가 사용됩니다.

HTTP 응답은 `catalog::NonImgExpiration`을(를) 기준으로 TTL을 사용하여 액세스할 수 있습니다.
